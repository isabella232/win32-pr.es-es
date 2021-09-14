---
title: Estructura FORMATETC
description: La estructura FORMATETC es un formato de Portapapeles generalizado, mejorado para abarcar un dispositivo de destino, un aspecto o vista de los datos y un medio de almacenamiento.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253113"
---
# <a name="the-formatetc-structure"></a>Estructura FORMATETC

La estructura FORMATETC es un formato generalizado del Portapapeles, mejorado para abarcar un dispositivo de destino, un aspecto o vista de los datos y un medio de almacenamiento.  Un consumidor de datos, como una aplicación contenedora OLE, pasa la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como argumento en las llamadas a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para indicar el tipo de datos que desea de un origen de datos, como un objeto de documento compuesto. El origen usa la **estructura FORMATETC** para describir qué formatos puede proporcionar.

[**FORMATETC puede**](/windows/win32/api/objidl/ns-objidl-formatetc) describir prácticamente cualquier dato, incluidos otros objetos como monikers. Un contenedor puede pedir a uno de sus objetos incrustados que enumere sus formatos de datos llamando a [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), que devuelve un objeto enumerador que implementa la interfaz [**IEnumFORMATETC.**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) En lugar de responder simplemente que tiene "texto y un mapa de bits", el objeto puede proporcionar una descripción detallada de los datos, incluido el dispositivo (normalmente pantalla o impresora) para el que se representa, el aspecto que se va a presentar al usuario (contenido completo, miniatura, icono o formato de impresión) y el medio de almacenamiento que contiene los datos (memoria global,  archivo de disco, objeto de almacenamiento o secuencia). Esta capacidad de describir estrechamente los datos dará como resultado una salida de pantalla y impresora de mayor calidad, así como una mayor eficacia en la exploración de datos, donde un boceto en miniatura es mucho más rápido de recuperar y mostrar que una representación totalmente detallada.

En la tabla siguiente se enumeran los campos de [**la estructura de datos FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y la información que especifican.



| Campo                   | Especifica                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Formato en el que se representarán los datos, que puede ser un formato estándar del Portapapeles, un formato propietario o un formato OLE. Para obtener más información sobre los formatos OLE, vea [Compound Documents](compound-documents.md).<br/>                                          |
| **Dpt**<br/>      | Una [**estructura DVTARGETDEVICE,**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) que contiene suficiente información sobre un dispositivo de destino de Windows, como una pantalla o impresora, para que se pueda crear un identificador para su contexto de dispositivo (hDC) mediante la [**función CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) <br/> |
| **dwAspect**<br/> | Aspecto o vista de los datos que se representan; puede ser el contenido completo, un boceto en miniatura, un icono o un formato para imprimir.<br/>                                                                                                                                  |
| **Lindex**<br/>   | La parte del aspecto que es de interés; para el presente, el valor debe ser -1, lo que indica que toda la vista es de interés.<br/>                                                                                                                                |
| **tymed**<br/>    | Medio de almacenamiento de los datos, que puede ser memoria global, archivo de disco o una instancia de una de las interfaces de almacenamiento estructurado de COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
</dt> </dl>

 

