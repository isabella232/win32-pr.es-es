---
description: Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se mostrarán en la interfaz de usuario Windows Explorer y dónde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usar listas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72289612d61ebfb198ec0f2ee3d4a7d206209e91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263031"
---
# <a name="using-property-lists"></a>Usar listas de propiedades

Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se mostrarán en la interfaz de usuario Windows Explorer y dónde. Hay varias ubicaciones donde las propiedades se muestran de solo lectura. Por otro lado, la edición de propiedades solo está habilitada en el **cuadro de diálogo** Propiedades. Ese cuadro de diálogo se puede invocar mediante el vínculo **Editar** propiedades del panel vista previa **o** el menú contextual de un elemento.

Las listas de propiedades son cadenas delimitadas por punto y coma que tienen el formato siguiente.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



La única marca disponible actualmente se muestra en la tabla siguiente.



| Marca | Descripción                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | No muestre la propiedad en el panel **vista** previa como se indica en el valor de clave del Registro **PreviewDetails.** Vea el ejemplo que sigue a la tabla siguiente si no se establece el valor de esa propiedad. |



 

Después de definir una lista de propiedades, puede almacenar esa cadena en el Registro a través del sistema de asociación de archivos de [Shell](../shell/fa-file-types.md) estándar en **HKEY \_ CLASSES \_ ROOT.** En la tabla siguiente se resumen los valores de las listas de propiedades que se pueden asignar en la clave del Registro para una extensión de nombre de archivo determinada.




| Value | Descripción | 
|-------|-------------|
| FullDetails | Las propiedades se muestran en la <strong>pestaña Detalles</strong> del cuadro <strong>de diálogo</strong> Propiedades . Esta es la lista completa de propiedades que admite el tipo de archivo. | 
| PreviewDetails | Las propiedades se muestran en el panel <strong>vista previa</strong>. | 
| PreviewTitle | Las propiedades se muestran en el área de título del panel <strong>vista</strong> previa junto a la miniatura del elemento. El número máximo de entradas es 3. Si la lista de propiedades contiene más del número máximo permitido, se omiten el resto de las entradas. | 
| TileInfo | Las propiedades se muestran cuando la vista de lista está en <strong>modo de vista</strong> Iconos. El número máximo de entradas es 3. Si la lista de propiedades contiene más del número máximo permitido, se omiten el resto de las entradas.<blockquote>[!Note]<br />Este valor estaba presente en Windows XP.</blockquote><br /> | 
| ExtendedTileInfo | Las propiedades se muestran para un elemento cuando la vista de lista está en <strong>modo de vista icono</strong> extendido. | 
| InfoTip | Las propiedades se muestran en una información general cuando un usuario mantiene el puntero sobre un elemento.<blockquote>[!Note]<br />Este valor estaba presente en Windows XP.</blockquote><br /> | 
| Información rápida | Las propiedades se muestran cuando es difícil recuperar propiedades directamente desde un elemento, como cuando se debe tener acceso al elemento a través de una conexión de red lenta. Se recomienda que las propiedades denominadas aquí, como Tipo o Tamaño, no requieran abrir la secuencia de archivos para determinar su valor.<blockquote>[!Note]<br />Este valor estaba presente en Windows XP.</blockquote><br /> | 




 

En el ejemplo siguiente se define el valor PreviewDetails para un tipo de archivo .recipe, mediante un ProgID de **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Como se explica en el tema [Asociación de archivos de Shell,](../shell/fa-file-types.md) las asociaciones de archivos se pueden describir para el formato más específico de la forma más general. El formulario más específico es la extensión de nombre de archivo único y el formulario más genérico es una clave que se aplica a todos los archivos y carpetas de archivos. Entre esos dos extremos, también puede definir un [PROGID](../shell/fa-progids.md) que agrupa un conjunto de extensiones de nombre de archivo (por ejemplo, los tipos .jpg y .jpeg agrupados como **jpegfile**). Al definir listas de propiedades, debe definirlas para ProgID o, en algunos casos, extensiones de nombre de archivo específicas. Evite confiar en entradas amplias, como la **clave AllFileSystemObjects.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
