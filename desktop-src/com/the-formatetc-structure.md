---
title: La estructura FORMATETC
description: La estructura FORMATETC es un formato de Portapapeles generalizado, que se ha mejorado para abarcar un dispositivo de destino, un aspecto o una vista de los datos, y un medio de almacenamiento.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794056"
---
# <a name="the-formatetc-structure"></a>La estructura FORMATETC

La estructura FORMATETC es un formato de Portapapeles generalizado, que se ha mejorado para abarcar un dispositivo de destino, un *aspecto* o una vista de los datos, y un medio de almacenamiento. Un consumidor de datos, como una aplicación contenedora OLE, pasa la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como argumento en las llamadas a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para indicar el tipo de datos que desea de un origen de datos, como un objeto de documento compuesto. El origen utiliza la estructura **FORMATETC** para describir los formatos que puede proporcionar.

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) puede describir prácticamente cualquier dato, incluidos otros objetos como monikers. Un contenedor puede solicitar a uno de sus objetos incrustados que muestren sus formatos de datos llamando a [**IDataObject:: del EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), que devuelve un objeto de enumerador que implementa la interfaz [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . En lugar de responder solo que tiene "texto y un mapa de bits", el objeto puede proporcionar una descripción detallada de los datos, incluido el dispositivo (normalmente la pantalla o la impresora) para el que se representa, el aspecto que se va a presentar al usuario (contenido completo, miniatura, icono o con formato para la impresión) y el medio de almacenamiento que contiene los datos (memoria global, archivo de disco, objeto de almacenamiento , o Stream). Esta capacidad para describir los datos de forma rigurosa, en el tiempo, da como resultado una impresora y una salida de pantalla de mayor calidad, así como más eficiencia en la exploración de datos, donde un boceto en miniatura es mucho más rápido de recuperar y mostrar que una representación totalmente detallada.

En la tabla siguiente se enumeran los campos de la estructura de datos [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y la información que especifican.



| Campo                   | Especifica                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Formato en el que se van a representar los datos, que pueden ser un formato de Portapapeles estándar, un formato de propietario o un formato de OLE. Para obtener más información sobre los formatos OLE, vea [documentos compuestos](compound-documents.md).<br/>                                          |
| **fichero**<br/>      | Una estructura [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) , que contiene suficiente información sobre un dispositivo de destino de Windows, como una pantalla o una impresora, de modo que se pueda crear un identificador para su contexto de dispositivo (HDC) con la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . <br/> |
| **dwAspect**<br/> | Aspecto o vista de los datos que se van a representar; puede ser todo el contenido, un boceto en miniatura, un icono o un formato para imprimir.<br/>                                                                                                                                  |
| **lindex**<br/>   | Parte del aspecto que es de interés; para el presente, el valor debe ser-1, lo que indica que toda la vista es de interés.<br/>                                                                                                                                |
| **tymed**<br/>    | Medio de almacenamiento de datos, que puede ser una memoria global, un archivo de disco o una instancia de una de las interfaces de almacenamiento estructurado de COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
</dt> </dl>

 

