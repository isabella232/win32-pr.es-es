---
description: Una llamada a la función PeerGroupSearchRecords requiere un parámetro de cadena de consulta XML que se utiliza para determinar los criterios básicos de una búsqueda.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Formato de consulta de búsqueda de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911625"
---
# <a name="record-search-query-format"></a><span data-ttu-id="a2172-103">Formato de consulta de búsqueda de registros</span><span class="sxs-lookup"><span data-stu-id="a2172-103">Record Search Query Format</span></span>

<span data-ttu-id="a2172-104">Una llamada a la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) requiere un parámetro de cadena de consulta XML que se utiliza para determinar los criterios básicos de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a2172-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="a2172-105">Use el esquema siguiente para formular una cadena XML:</span><span class="sxs-lookup"><span data-stu-id="a2172-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="a2172-106">Elementos que se van a usar para una búsqueda de registros</span><span class="sxs-lookup"><span data-stu-id="a2172-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="a2172-107">El elemento principal de una búsqueda de registros es **peersearch**, que contiene el identificador uniforme de recursos (URI) del esquema asociado en el atributo **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="a2172-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="a2172-108">Cuando **peersearch** se usa como un elemento secundario, puede usar los elementos **y**, la **cláusula** y **o** como elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a2172-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="a2172-109">**y** : el elemento **y** realiza una operación and lógica en una o más cláusulas contenidas entre las etiquetas de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="a2172-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="a2172-110">Otras etiquetas **and** y **or** pueden ser elementos secundarios, y los resultados recursivos de sus cláusulas secundarias se incluyen en la operación.</span><span class="sxs-lookup"><span data-stu-id="a2172-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="a2172-111">Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters y una última actualización mayor que 2/28/2003, o una fecha de creación inferior a 1/31/2003, use la siguiente cadena de consulta XML:</span><span class="sxs-lookup"><span data-stu-id="a2172-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="a2172-112">**cláusula** : el elemento de la **cláusula** especifica una regla comparativa básica que compara el valor de un atributo de registro específico con el valor incluido entre las etiquetas de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="a2172-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="a2172-113">Se **deben proporcionar los** atributos **Type** y **Compare** para indicar la operación de comparación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="a2172-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="a2172-114">Por ejemplo, una búsqueda simple que indica que todos los registros coincidentes deben tener un valor de **peercreatorid** igual a James Peters aparece en la cadena de consulta XML como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a2172-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="a2172-115">Los atributos de **tipo** comunes son **int**, **String** y **Date**.</span><span class="sxs-lookup"><span data-stu-id="a2172-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="a2172-116">El atributo **Date** puede ser uno de los formatos de fecha estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="a2172-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="a2172-117">Los valores del atributo **Compare** son **Equal**, **notequal**, **less**, **Greater**, **lessorequal** y **greaterorequal**.</span><span class="sxs-lookup"><span data-stu-id="a2172-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="a2172-118">**o** bien-el elemento **o** realiza una operación OR lógica en una o más cláusulas contenidas entre las etiquetas de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="a2172-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="a2172-119">Los elementos **o** y **y** pueden ser elementos secundarios, y los resultados recursivos de las cláusulas secundarias se incluyen en la operación.</span><span class="sxs-lookup"><span data-stu-id="a2172-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="a2172-120">Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters, o una última actualización entre 1/31/2003 y 2/28/2003, use la siguiente cadena de consulta XML:</span><span class="sxs-lookup"><span data-stu-id="a2172-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="a2172-121">Más información acerca de una búsqueda de registros</span><span class="sxs-lookup"><span data-stu-id="a2172-121">More Information About a Record Search</span></span>

<span data-ttu-id="a2172-122">El primer nivel de nodos después de **peersearch** solo puede tener un elemento.</span><span class="sxs-lookup"><span data-stu-id="a2172-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="a2172-123">Sin embargo, los elementos secundarios posteriores de ese elemento pueden tener muchos elementos en el mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="a2172-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="a2172-124">La siguiente consulta de búsqueda es incorrecta:</span><span class="sxs-lookup"><span data-stu-id="a2172-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="a2172-125">Se produce un error en la consulta porque se devuelven dos valores para la coincidencia sin resolverse en un valor true/false, lo que significa que una cláusula es una consulta para el nombre de un registro que es igual a James Peters, y la operación y coincide con las dos cláusulas de componentes.</span><span class="sxs-lookup"><span data-stu-id="a2172-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="a2172-126">El resultado son dos valores lógicos verdadero/falso que son contradictorios.</span><span class="sxs-lookup"><span data-stu-id="a2172-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="a2172-127">Para obtener todos los registros que contienen un nombre igual a James Peters y una última actualización entre 1/31/2003 y 2/28/2003, coloque la **cláusula** y las etiquetas que estén en el mismo nivel entre la apertura y el cierre **y** **las etiquetas.**</span><span class="sxs-lookup"><span data-stu-id="a2172-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="a2172-128">En el ejemplo siguiente se muestra la consulta correcta:</span><span class="sxs-lookup"><span data-stu-id="a2172-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="a2172-129">En la siguiente lista se identifica otra información específica que debe saber para escribir una consulta correcta:</span><span class="sxs-lookup"><span data-stu-id="a2172-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="a2172-130">Las etiquetas **and** y **or** no se pueden encontrar entre las etiquetas de la **cláusula** de apertura y de cierre porque, en esa configuración, se interpretan como parte del valor con el que debe coincidir, lo que genera un error o una coincidencia con errores.</span><span class="sxs-lookup"><span data-stu-id="a2172-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="a2172-131">Cada par de etiquetas **and** y **or** y de apertura y cierre deben incluir al menos uno o más nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a2172-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="a2172-132">No se permite un conjunto de elementos cero en este esquema.</span><span class="sxs-lookup"><span data-stu-id="a2172-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="a2172-133">Atributos de registro</span><span class="sxs-lookup"><span data-stu-id="a2172-133">Record Attributes</span></span>

<span data-ttu-id="a2172-134">Mediante el uso del [esquema de atributo de registro](record-attribute-schema.md), un usuario puede crear atributos de registro que el atributo **attrib** XML de un elemento de la cláusula especifique.</span><span class="sxs-lookup"><span data-stu-id="a2172-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="a2172-135">Los atributos de un nuevo registro se agregan estableciendo el miembro **pszAttributes** del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) en una cadena XML con el formato especificado en el esquema.</span><span class="sxs-lookup"><span data-stu-id="a2172-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="a2172-136">La infraestructura del mismo nivel reserva los siguientes nombres de atributo:</span><span class="sxs-lookup"><span data-stu-id="a2172-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="a2172-137">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="a2172-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="a2172-138">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="a2172-138">**peercreatorid**</span></span>
-   <span data-ttu-id="a2172-139">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="a2172-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="a2172-140">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="a2172-140">**peerrecordid**</span></span>
-   <span data-ttu-id="a2172-141">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="a2172-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="a2172-142">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="a2172-142">**peercreationtime**</span></span>
-   <span data-ttu-id="a2172-143">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="a2172-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="a2172-144">Caracteres especiales</span><span class="sxs-lookup"><span data-stu-id="a2172-144">Special Characters</span></span>

<span data-ttu-id="a2172-145">Algunos caracteres se pueden usar para expresar patrones de coincidencia o para aplicar un carácter de escape a otros caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="a2172-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="a2172-146">Estos caracteres se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2172-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="a2172-147">Patrón de caracteres</span><span class="sxs-lookup"><span data-stu-id="a2172-147">Character pattern</span></span> | <span data-ttu-id="a2172-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2172-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="a2172-149">Carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="a2172-149">The wildcard character.</span></span> <span data-ttu-id="a2172-150">Cuando este carácter se encuentra en un valor de la cláusula, coincide con 0-n caracteres de cualquier valor, incluidos los caracteres de espacio en blanco y no alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="a2172-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="a2172-151">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a2172-151">For example:</span></span><br/> <span data-ttu-id="a2172-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="a2172-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="a2172-153">Esta cláusula coincide con todos los valores de **peercreatorid** con el nombre "James" y el apellido que empieza por "P".</span><span class="sxs-lookup"><span data-stu-id="a2172-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="a2172-154">Asterisco con escape.</span><span class="sxs-lookup"><span data-stu-id="a2172-154">An escaped asterisk.</span></span> <span data-ttu-id="a2172-155">Esta secuencia coincide con un carácter de asterisco.</span><span class="sxs-lookup"><span data-stu-id="a2172-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a2172-156">?</span><span class="sxs-lookup"><span data-stu-id="a2172-156">?</span></span>                 | <span data-ttu-id="a2172-157">Carácter comodín de un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="a2172-157">The single-character wildcard character.</span></span> <span data-ttu-id="a2172-158">Cuando este carácter se encuentra en un valor de la cláusula, coincide con cualquier carácter individual, incluidos los caracteres de espacio en blanco y no alfanuméricos. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a2172-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="a2172-159">"<clause attrib="filename" type="string" compare="equal">Data-0?. XML</clause>"</span><span class="sxs-lookup"><span data-stu-id="a2172-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="a2172-160">Esta cláusula coincide con los valores de **nombre de archivo** como "data-01.xml" y "data-0B.xml".</span><span class="sxs-lookup"><span data-stu-id="a2172-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="a2172-161">\\?</span><span class="sxs-lookup"><span data-stu-id="a2172-161">\\?</span></span>               | <span data-ttu-id="a2172-162">Un signo de interrogación de escape.</span><span class="sxs-lookup"><span data-stu-id="a2172-162">An escaped question mark.</span></span> <span data-ttu-id="a2172-163">Esta secuencia coincide con un carácter de signo de interrogación.</span><span class="sxs-lookup"><span data-stu-id="a2172-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="a2172-164">Una barra diagonal inversa con escape.</span><span class="sxs-lookup"><span data-stu-id="a2172-164">An escaped backslash.</span></span> <span data-ttu-id="a2172-165">Esta secuencia coincide con un único carácter de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a2172-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="a2172-166">Si la secuencia de caracteres no es válida, la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) devuelve el error **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="a2172-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="a2172-167">Una secuencia no válida es cualquier secuencia que contenga un \\ carácter "" (barra diagonal inversa) no seguido inmediatamente de un \* carácter "" (asterisco), una "?" (signo de interrogación), u otro \\ carácter "" (barra diagonal inversa).</span><span class="sxs-lookup"><span data-stu-id="a2172-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




