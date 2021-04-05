---
description: Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se deben mostrar en la interfaz de usuario del explorador de Windows y dónde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usar listas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001576"
---
# <a name="using-property-lists"></a>Usar listas de propiedades

Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se deben mostrar en la interfaz de usuario del explorador de Windows y dónde. Hay varias ubicaciones en las que las propiedades se muestran en modo de solo lectura. Por otro lado, la edición de propiedades solo está habilitada en el cuadro de diálogo **propiedades** . Ese cuadro de diálogo se puede invocar a través del vínculo **Editar propiedades** en el **Panel de vista previa** o en el menú contextual de un elemento.

Las listas de propiedades son cadenas delimitadas por punto y coma que tienen el formato siguiente.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



La única marca disponible actualmente se muestra en la tabla siguiente.



| Marca | Descripción                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | No muestre la propiedad en el **Panel de vista previa** como se indica en el valor de la clave del registro **PreviewDetails** . Vea el ejemplo que sigue a la siguiente tabla si no se establece el valor de esa propiedad. |



 

Después de definir una lista de propiedades, puede almacenar esa cadena en el registro a través del sistema de [asociaciones de archivo de Shell](../shell/fa-file-types.md) estándar en **HKEY \_ classes \_ root.** En la tabla siguiente se resumen los valores de las listas de propiedades que se pueden asignar en la clave del registro para una extensión de nombre de archivo determinada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FullDetails</td>
<td>Las propiedades se muestran en la pestaña <strong>detalles</strong> del cuadro de diálogo <strong>propiedades</strong> . Esta es la lista completa de propiedades que admite el tipo de archivo.</td>
</tr>
<tr class="even">
<td>PreviewDetails</td>
<td>Las propiedades se muestran en el <strong>Panel de vista previa</strong>.</td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>Las propiedades se muestran en el área de título del <strong>Panel de vista previa</strong> junto a la miniatura del elemento. El número máximo de entradas es 3. Si la lista de propiedades contiene más del número máximo permitido, se omite el resto de las entradas.</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>Las propiedades se muestran cuando la vista de lista está en modo de vista en <strong>mosaico</strong> . El número máximo de entradas es 3. Si la lista de propiedades contiene más del número máximo permitido, se omite el resto de las entradas.
<blockquote>
[!Note]<br />
Este valor estaba presente en Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>ExtendedTileInfo</td>
<td>Las propiedades se muestran para un elemento cuando la vista de lista está en modo de vista de <strong>mosaico extendido</strong> .</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>Las propiedades se muestran en un recuadro informativo cuando un usuario mantiene el mouse sobre un elemento.
<blockquote>
[!Note]<br />
Este valor estaba presente en Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickTip</td>
<td>Las propiedades se muestran cuando es difícil recuperar propiedades directamente de un elemento, como cuando se debe tener acceso al elemento a través de una conexión de red lenta. Se recomienda que las propiedades mencionadas aquí, como tipo o tamaño, no requieran abrir el flujo de archivo para determinar su valor.
<blockquote>
[!Note]<br />
Este valor estaba presente en Windows XP.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

En el ejemplo siguiente se define el valor de PreviewDetails para un tipo de archivo. Recipe mediante un ProgID de **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Como se explica en el tema [Asociación de archivos de Shell](../shell/fa-file-types.md) , las asociaciones de archivo se pueden describir para el formato más específico del más general. La forma más específica es la extensión de nombre de archivo única y la forma más genérica es una clave que se aplica a todos los archivos y carpetas de archivos. Entre esos dos extremos, también puede definir un [ProgID](../shell/fa-progids.md) que agrupe un conjunto de extensiones de nombre de archivo (por ejemplo, los tipos. jpg y. JPEG agrupados como **jpegfile**). Al definir las listas de propiedades, debe definirlas para los ProgID o, en algunos casos, las extensiones de nombre de archivo específicas. Evite depender de entradas amplias, como la clave **AllFileSystemObjects** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
