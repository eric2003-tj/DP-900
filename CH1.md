<h1> Microsoft Azure 資料基本概念：探索核心資料概念 </h1>
<h2>學習目標</h3>
<ul>
  <li>确定常见数据格式</li>
  <li>描述用于在文件中存储数据的选项</li>
  <li>描述用于在数据库中存储数据的选项</li>
  <li>描述事务数据处理解决方案的特征</li>
  <li>描述分析数据处理解决方案的特征</li>
</ul>
<h2>确定数据格式</h3>
<ol>
  <li>结构化数据</li>
  <li>半结构化数据</li>
  <li>结构化数据</li>
</ol>
<h3>結構化資料</h3>
<p>结构化数据是遵循固定架构的数据，因此所有数据都具有相同的字段或属性。 结构化数据实体的架构通常是表格</p>
<img src = "https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/2-tabular-diagram.png">
<h3>半結構化資料</h3>
<p>半结构化数据是指具有某种结构的信息，但它允许实体实例之间存在一些变化。 例如，虽然大多数客户可能都有电子邮件地址，但有些可能有多个电子邮件地址，而有些可能根本没有。
一种常见的半结构化数据格式是 JavaScript 对象表示法 (JSON)。 下面的示例显示了两个表示客户信息的 JSON 文档。 每个客户文档都包含地址和联系人信息，但具体字段因客户而异。</p>
<img src ="https://github.com/eric2003-tj/DP-900/blob/main/json.png">
<h3>非結構性資料</h3>
<p>並非所有資料都是結構化，甚至是半結構化。 例如，文档、图像、音频和视频数据以及二进制文件可能没有特定的结构。 此类数据称为非结构化数据。</p>
<h2>資料存放區</h2>
<p>组织通常以结构化、半结构化或非结构化格式存储数据，用于记录实体（例如客户和产品）、特定事件（例如销售交易）的详细信息以及文档、图像和其他格式的其他信息。 然后可以检索存储的数据，以供以后分析和报告。
  <br>
常用的数据存储分为两大类：</p>
<ul>
  <li>文件存储</li>
  <li>資料庫</li>
</ul>
<h2>探索檔案儲存體</h2>
<p>將資料儲存在檔案中的能力是任何運算系統的核心元素。 檔案可以儲存在個人電腦硬碟上的本機檔案系統，以及 USB 隨身碟抽取式媒體上；但在多數組織中，重要資料檔會集中儲存在某些類型的共用檔案儲存系統中。 中央儲存位置會逐漸裝載至雲端，為大量資料提供符合成本效益、安全且可靠的儲存空間。</p>
<p>用來儲存資料的特定檔案格式取決於許多因素，包括：</p>
<ul>
  <li>儲存的資料類型 (結構化、半結構化或非結構化)。</li>
  <li>需要讀取、寫入及處理資料的應用程式與服務。</li>
  <li>需要讓人類可讀的資料檔，或針對有效率的儲存和處理進行最佳化。</li>
</ul>
<h3>分隔的文字檔案</h3>
<p>資料通常會以純文字格式儲存，並具有特定的欄位分隔符號和列結束字元。 分隔資料最常見的格式是逗點分隔值檔案 (CSV)，其中的欄位會以逗號分隔，而列則以歸位字元/新行終止。 (選擇性) 第一行可能包括欄位名稱。 其他常用格式包括定位字元分隔值 (TSV) 和空格分隔 (使用索引標籤或空格來分隔欄位)，以及將每個欄位配置固定字元數的固定寬度資料。 針對需要以一般人看得懂的格式存取、各種應用程式和服務的結構化資料，分隔符號文字是個好選擇。</p>
<img src = "https://docs.microsoft.com/en-us/power-query/combine-files-csv">
<h3>JavaScript 物件標記法 (JSON)</h3>
<p>JSON 是一種普遍的格式，階層式檔案結構描述可用來定義具有多個屬性的資料實體 (物件)。 每個屬性可能是物件 (或物件集合)；讓 JSON 成為適合結構化及半結構化資料的彈性格式。</p>
<img src ="https://github.com/eric2003-tj/DP-900/blob/main/json.png">
<h3>可延伸標記語言 (XML)</h3>
<p>XML 是一種一般人看得懂的資料格式，在 1990 和 2000 年代很受歡迎。 這主要是由較不詳細的 JSON 格式取代，但仍有一些系統使用 XML 來代表資料。 XML 使用以角括弧括住的標籤 (<../>)，以定義元素和屬性，如下列範例所示：</p>
<img src = "https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/RecipeBook_XML_Example.svg/425px-RecipeBook_XML_Example.svg.png">
<h3>二進位大型物件 (BLOB)</h3>
<p>最後，所有檔案都會儲存為二進位資料 (1 和 0)，但在上述討論的人類可讀的格式中，二進位資料的位元組會對應至可列印的字元 (通常是透過如 ASCII 或 Unicode 等字元編碼配置)。 不過某些檔案格式 (尤其是非結構化資料) 會將資料儲存為原始二進位，而這些二進位檔案必須由應用程式轉譯並呈現。 儲存為二進位檔案的常見資料類型包括影像、視訊、音訊和應用程式特定的文件。
使用這類資料時，資料專業人員通常會將資料檔案稱為 BLOB (二進位大型物件)。</p>
<h3>最佳化檔案格式</h3>
<p>雖然結構化及半結構化資料的人類可讀格式很有用，但通常不會針對儲存空間或處理進行最佳化。 經過一段時間，我們開發了一些特殊的檔案格式，可進行壓縮、編編製索引，以及有效儲存和處理。
您可能會看到一些常見的最佳化檔案格式，包括 Avro、ORC 和 Parquet：</p>
<ul>
  <li>Avro 是以資料列為基礎的格式。 其是由 Apache 所建立。 每一筆記錄都包含一個標頭，描述記錄中資料的結構。 此標頭會儲存為 JSON。 資料會儲存為二進位資訊。 應用程式會使用標頭中的資訊來剖析二進位資料，並擷取其包含的欄位。 Avro 是非常適合用來壓縮資料，並將儲存體和網路頻寬需求降至最低的格式。
</li>
  <li>ORC (最佳化的資料列單欄式格式) 可將資料組織成資料行，而不是資料列。 它是由 HortonWorks 開發，用於最佳化 Apache Hive 的讀取和寫入作業 (Apache Hive 是一種資料倉儲系統，可支援對大型資料集進行快速的資料摘要和查詢)。 ORC 檔案包含「等量」資料。 每個等量都會保留一個或一組資料行的資料。 等量包含等量中資料列的索引、每個資料列的資料，以及一個頁尾，其中保留每個資料行的統計資訊 (計數、總和、最大值、最小值等)。
</li>
  <li>Parquet 是另一個單欄式資料格式。 其是由 Cloudera 和 Twitter 所建立。 Parquet 檔案包含資料列群組。 每個資料行的資料會一起儲存在同一資料列群組中。 每個資料列群組都包含一或多個資料區塊。 Parquet 檔案包含中繼資料，描述在每個區塊中找到的一組資料列。 應用程式可以使用此中繼資料來快速找出一組指定資料列的正確區塊，並針對這些資料列擷取指定資料行中的資料。 Parquet 專門用來有效率地儲存和處理巢狀資料類型。 其支援非常有效率的壓縮和編碼配置。</li>
</ul>
<h2>探索資料庫</h2>
<p>資料庫可用來定義中央系統，以便在其中儲存和查詢資料。 簡單而言，儲存檔案的檔案系統是一種資料庫；但在專業資料內容中使用這個名詞時，我們通常指的是用來管理資料記錄 (而非檔案) 的專用系統。</p>
<h3>關聯式資料庫</h3>
<p>關聯式資料庫通常用來儲存和查詢結構化資料。 資料會儲存在代表實體 (例如客戶、產品或銷售訂單) 的資料表中。 實體的每個執行個體都會獲指派可唯一加以識別的主索引鍵，且這些索引鍵可用來在其他資料表中參考該實體執行個體。 例如，可以在銷售訂單記錄中參考客戶的主索引鍵，以指出有哪些客戶已下訂單。 使用索引鍵來參考資料實體的做法，能使關聯式資料庫標準化；意思是能去除重複的資料值。因此舉例來說，個別客戶的詳細資料只會儲存一次，而不會因為客戶多次下訂單而儲存多次。 資料表是使用結構化查詢語言 (SQL) 來管理和查詢。SQL 是以 ANSII 標準為基礎，因此在多個資料庫系統上都會很類似。</p>
<img src="https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/relational-database.png">
<h3>非關聯式資料庫</h3>
<p>非關聯式資料庫是不會將關聯式結構描述套用至資料的資料管理系統。 非關聯式資料庫通常稱為 NoSQL 資料庫，不過某些非關聯式資料庫仍然能夠支援 SQL 語言的變體。</p>
<ul>
  <li><strong>索引鍵/值資料庫</strong>，其中每個記錄都包含唯一索引鍵和相關聯的值，可以是任何格式。</li>
  <br>
  <img src ="https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/key-value-store.png">
  <li><strong>文件資料庫</strong>，這是索引鍵/值資料庫的特定形式，其值為 JSON 文件 (系統最佳化以剖析和查詢)
</li>
  <br>
  <img src ="https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/document-store.png">
  <li><strong>資料行系列資料庫</strong>，會儲存表格式資料，其中包含資料列和資料行，但是您可以將這些資料行分割成稱為資料行系列的群組。 每個資料行系列都會保留一組邏輯上相關的資料行。</li>
  <br>
  <img src = "https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/column-family-store.png">
  <li><strong>圖形資料庫</strong>，會將實體儲存為具有連結的節點，以定義實體之間的關聯性。</li>
  <br>
  <img src = "https://docs.microsoft.com/zh-tw/learn/wwl-data-ai/explore-core-data-concepts/media/graph.png">
</ul>
<br>
<h3>OLTP</h3>
<p>用於關聯式資料庫的交易需符合ACID原則</p>
<ol>
  <li>原子性(Atomicity)</li>
  <li>一致性(Consistency)</li>
  <li>隔離性(Isolation)</li>
  <li>持久性(Durability)</li>
</ol>
<br>
<h3>OLAP</h3>
<p>There are three steps dealing with dataset</p>
<ul>
  <li>Extract dataset</li>
  <li>Transform(Normalization,formation...) dataset</li>
  <li>Load dataset</li>
</ul>
<p>It is often used in non-relational dataset like NoSQL's ELT/ETL processing.
Data is loaded,arranged and then strored in cube.Furthermore, it can be used in data analysis and decision making.</p>
<ul>
  <li>summary</li>
  <li>trend</li>
  <li>BI(business intelligence</li>
</ul>
<p>We can use batch arrangement(not immediately) and stream arrangement(immediately)</p>
