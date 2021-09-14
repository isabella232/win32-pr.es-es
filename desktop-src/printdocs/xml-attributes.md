---
description: Obtenga información sobre los atributos XML en el marco de esquema de impresión. Este tema no está al día. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa19a64dd5d3c59f7c5d26b86186912065a5f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248366"
---
# <a name="xml-attributes"></a>Atributos XML

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Hay una serie de atributos XML que aparecen en varios tipos de elementos definidos en el marco de esquema de impresión. Los atributos XML con el mismo nombre suelen tener el mismo significado y cumplir las mismas reglas, independientemente del tipo de elemento en el que residen. Por lo tanto, los atributos XML se enumeran aquí por nombre y no por su tipo de elemento host. No se permiten atributos XML definidos de forma privada. Solo los atributos XML definidos aquí se pueden usar en un documento PrintCapabilities o printTicket y, a continuación, solo en el contexto definido.

Aunque no se permite a las partes privadas introducir nuevas definiciones en el espacio de nombres de otra parte, se les permite usar nombres existentes de otro espacio de nombres privado, siempre y cuando su uso sea coherente con el uso establecido por la otra parte. Por lo tanto, una opción puede contener elementos ScoredProperty definidos por varias partes diferentes, cada una de las que residen en espacios de nombres diferentes.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nombre del atributo</th>
<th>Tipos de datos y valores</th>
<th>Propósito</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>XML QName<br/></td>
<td>Este atributo XML identifica la instancia del elemento. Distingue un elemento de otro del mismo tipo de elemento. Este atributo XML se usa tanto que se conoce como el atributo name.<br/></td>
<td>Las restricciones siguientes pertenecen al atributo name.<br/>
<ul>
<li>El atributo name debe tener el formato de un QName válido definido por XML. Es decir, debe estar calificado por un espacio de nombres XML válido. Los QNames que aparecen como valores de atributos de nombre deben estar calificados explícitamente como espacio de nombres, incluso si se define un espacio de nombres predeterminado. <br/></li>
<li>El contenido de caracteres debe ser el de un QName válido definido por XML. <br/></li>
<li>Los nombres definidos de forma privada deben calificarse con un espacio de nombres que esté asociado de forma única a la entidad que presentó el atributo name.<br/></li>
<li>Requisito de unidad del mismo nivel: no dos elementos del mismo nivel que pertenecen al mismo tipo de elemento pueden tener el mismo atributo de nombre. La única excepción son los elementos Option, donde el atributo name se puede usar para definir una opción. Por lo tanto, los elementos Option de varios elementos del mismo nivel pueden tener el mismo atributo de nombre.<br/></li>
<li>Los siguientes tipos de elemento pueden contener atributos de nombre: Property, ScoredProperty, ParameterDef, Option y Feature.<br/></li>
<li>Los atributos name deben aparecer en cada uno de los tipos de elemento que los contienen, excepto en el caso de algunos elementos de opción de esquema de impresión público definidos previamente, como DocumentNUp.<br/></li>
</ul>
En el ejemplo siguiente se muestra cómo identificar una instancia de Option mediante un atributo 'name'. Esta es la manera correcta de definir elementos Option. Un proveedor no debe tener opciones sin nombre, a menos que estén definidas públicamente en el esquema de impresión, como DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  &lt;/psf:Option&gt;</code></pre></td>
</tr>
<tr class="even">
<td>Propagar <br/></td>
<td>Enumeración<br/> Actualmente no hay ningún valor definido.<br/></td>
<td>El atributo propagate no se usa en la versión inicial de Print Schema Framework. Se documenta aquí para que el código de validación PrintCapabilities o PrintTicket implementado para la versión inicial de Print Schema Framework pueda procesar cualquier versión de esquema posterior sin errores.<br/></td>

</tr>
<tr class="odd">
<td>Limitada <br/></td>
<td>Enumeración<br/> Valores permitidos:<br/>
<ul>
<li>None <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indica si la opción está disponible para su selección o para su uso. <br/></td>
<td>Los valores permitidos del atributo restringido tienen los significados siguientes. Tenga en cuenta que estos valores se muestran en orden, de menos restrictivo (Ninguno) a más restrictivo (DeviceSettings).<br/> None <br/>
<ul>
<li>La opción no está restringida. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>La opción está restringida por la configuración de PrintTicket. Esto implica que cambiar la configuración puede quitar la restricción. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>La opción está restringida por la configuración del administrador; El usuario no puede habilitar la opción .<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>La opción está restringida por la configuración del dispositivo o las opciones de dispositivo instaladas físicamente; El usuario o el administrador no pueden habilitar la opción.<br/></li>
</ul>
Cuando el proveedor PrintCapabilities notifica los valores del atributo restringido, se debe notifica la restricción más restrictiva encontrada. Por ejemplo, si una opción está restringida por una configuración de administrador y una configuración de dispositivo, el proveedor PrintCapabilities debe notificar DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>Identificador URI<br/></td>
<td>Este atributo XML establece un vínculo entre un identificador uniforme de recursos (URI) de espacio de nombres y el prefijo de espacio de nombres que aparece en el QName XML. Debe establecer este vínculo al URI del espacio de nombres definido para el marco de esquema de impresión para poder usar cualquiera de las etiquetas de elemento definidas por el marco, atributos, atributos de nombre, y así sucesivamente. Puede declarar este espacio de nombres como predeterminado para evitar calificar realmente las etiquetas de elemento con un prefijo de espacio de nombres, aunque todos los demás QNames deben calificarse explícitamente. El espacio de nombres estándar debe definirse en el elemento raíz adecuado. Observe todas las reglas y convenciones XML relacionadas con el uso del atributo xmlns.<br/> El URI del marco de esquema de impresión es http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> El URI de las palabras clave de esquema de impresión es https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




