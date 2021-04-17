---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105689710"
---
# <a name="xml-attributes"></a>Atributos XML

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Hay una serie de atributos XML que aparecen en varios tipos de elemento definidos en el marco de trabajo del esquema de impresión. Los atributos XML con el mismo nombre generalmente tienen el mismo significado y obedecen a las mismas reglas independientemente del tipo de elemento en el que residen. Por lo tanto, los atributos XML se enumeran aquí por nombre y no por su tipo de elemento host. No se permiten atributos XML definidos de forma privada. Solo los atributos XML definidos aquí se pueden usar en un documento de PrintCapabilities o en un PrintTicket y solo en el contexto definido.

Aunque los usuarios privados no pueden introducir nuevas definiciones en el espacio de nombres de otra entidad, se les permite usar los nombres existentes de otro espacio de nombres privado, siempre que su uso sea coherente con el uso establecido por la otra parte. Por lo tanto, una opción puede contener elementos ScoredProperty definidos por varias partes diferentes, cada uno de los cuales reside en diferentes espacios de nombres.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td>QName XML<br/></td>
<td>Este atributo XML identifica la instancia del elemento. Distingue un elemento de otro del mismo tipo de elemento. Este atributo XML es tan ampliamente utilizado y se conoce como atributo de nombre.<br/></td>
<td>Las siguientes restricciones se aplican al atributo name.<br/>
<ul>
<li>El atributo name debe tener el formato de un QName válido definido por XML. Es decir, debe estar calificado por un espacio de nombres XML válido. Los QNames que aparecen como valores de los atributos name deben ser explícitamente calificados con el espacio de nombres aunque se haya definido un espacio de nombres predeterminado. <br/></li>
<li>El contenido del carácter debe ser el de un QName válido definido por XML. <br/></li>
<li>Los nombres definidos de forma privada se deben calificar con un espacio de nombres que esté asociado de manera única a la entidad que presentó el atributo de nombre.<br/></li>
<li>Requisito de unicidad relacionado: no dos elementos del mismo nivel que pertenezcan al mismo tipo de elemento pueden tener el mismo atributo de nombre. La única excepción son los elementos Option, donde el atributo name se puede usar para definir una opción. Por lo tanto, los elementos de opción de varios nodos pueden tener el mismo atributo de nombre.<br/></li>
<li>Los siguientes tipos de elemento pueden contener atributos de nombre: Property, ScoredProperty, ParameterDef, Option y Feature.<br/></li>
<li>los atributos name deben aparecer en cada uno de los tipos de elemento que los contengan, excepto en el caso de algunos elementos de opción de esquema de impresión pública definidos anteriormente, como DocumentNUp.<br/></li>
</ul>
En el ejemplo siguiente se muestra cómo identificar una instancia de opción mediante un atributo ' name '. Esta es la manera correcta de definir elementos Option. Un proveedor no debe tener opciones sin nombre, a menos que estén definidas públicamente en el esquema de impresión, como DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td>propagar <br/></td>
<td>Enumeración<br/> No hay ningún valor definido actualmente.<br/></td>
<td>El atributo Propagate no se utiliza en la versión inicial del marco de trabajo del esquema de impresión. Se documenta aquí para que el código de validación de PrintCapabilities o PrintTicket implementado para la versión inicial del marco de trabajo del esquema de impresión pueda procesar cualquier versión de esquema posterior sin errores.<br/></td>

</tr>
<tr class="odd">
<td>restringida <br/></td>
<td>Enumeración<br/> Valores permitidos:<br/>
<ul>
<li>None <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indica si la opción está disponible para la selección o para su uso. <br/></td>
<td>Los valores permitidos del atributo Constrained tienen los significados siguientes. Tenga en cuenta que estos valores se muestran en orden, de menos restrictivo (ninguno) a más restrictiva (DeviceSettings).<br/> None <br/>
<ul>
<li>La opción no está restringida. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>La opción está restringida por la configuración de PrintTicket. Esto implica que el cambio de la configuración puede quitar la restricción. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>La opción está restringida por la configuración del administrador; el usuario no puede habilitar la opción.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>La opción está restringida por la configuración del dispositivo o las opciones del dispositivo instalado físicamente. el usuario o el administrador no pueden habilitar la opción.<br/></li>
</ul>
Cuando el proveedor de PrintCapabilities informa de los valores del atributo restringido, se debe notificar la restricción más restrictiva encontrada. Por ejemplo, si una opción está restringida por una configuración de administrador y una configuración de dispositivo, el proveedor de PrintCapabilities debe notificar a DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Este atributo XML establece un vínculo entre un identificador uniforme de recursos (URI) de espacio de nombres y el prefijo de espacio de nombres que aparece en el QName XML. Debe establecer este tipo de vínculo con el identificador URI de espacio de nombres definido para el marco de trabajo del esquema de impresión antes de poder usar cualquiera de las etiquetas de elementos definidas por el marco, atributos, atributos de nombre, etc. Puede declarar este espacio de nombres para que sea el valor predeterminado para evitar que las etiquetas de elementos se califiquen realmente con un prefijo de espacio de nombres, aunque todos los demás QNames deben estar explícitamente calificados. El espacio de nombres estándar debe definirse en el elemento raíz adecuado. Observe todas las reglas y convenciones XML con respecto al uso del atributo xmlns.<br/> El URI para el marco de trabajo del esquema de impresión es http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> El URI de las palabras clave del esquema de impresión es https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




