---
title: Interfaces de Transferencia de datos
description: Interfaces de Transferencia de datos
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714467"
---
# <a name="data-transfer-interfaces"></a>Interfaces de Transferencia de datos

La interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) proporciona a los consumidores de datos métodos para obtener y establecer los datos de un objeto, determinar qué formatos admite el objeto y registrar y recibir notificaciones cuando cambian los datos en el objeto. Al obtener datos, un llamador puede especificar el formato en el que desea representar los datos. El origen de los datos, sin embargo, determina el medio de almacenamiento, que devuelve en un parámetro out proporcionado por el autor de la llamada.

Por sí solo, [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) proporciona todas las herramientas que necesita para implementar las transferencias del portapapeles de Windows o las transferencias de documentos compuestos en sus aplicaciones. Si también desea admitir las transferencias de arrastrar y colocar, debe implementar las interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) junto con **IDataObject**.

La interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinada con las API del portapapeles OLE proporciona todas las capacidades de las API del portapapeles de Windows. Por lo general, no es necesario usar ambas API del portapapeles. Los proveedores de datos que admiten transferencias de arrastrar y colocar o documentos compuestos OLE deben implementar la interfaz **IDataObject** . Si la aplicación solo admite las transferencias del portapapeles, pero tiene previsto agregar documentos de arrastrar y colocar o compuestos en versiones posteriores, puede que desee implementar **IDataObject** y las API del portapapeles OLE ahora para minimizar la cantidad de tiempo empleado en la recodificación y depuración más adelante. También puede implementar **IDataObject** para usar medios de transferencia distintos de la memoria global.

En la tabla siguiente se resumen las opciones que se deben usar, en función de los tipos de transferencia de datos que desee admitir:



| Para admitir                                                                       | Use                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documentos compuestos<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Arrastrar y colocar transferencias<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (o el equivalente)<br/> |
| Transferencias del portapapeles mediante la memoria global exclusivamente<br/>                   | [API del portapapeles](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Transferencias del Portapapeles con medios de Exchange distintos de la memoria global.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| El portapapeles transfiere ahora, pero arrastra y coloca o documentos compuestos posteriormente<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y las interfaces y funciones enumeradas anteriormente para "arrastrar y colocar transferencias"<br/>                                                    |



 

Cuando un usuario inicia una operación de transferencia de datos, la aplicación de origen crea una instancia de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y, a su vez, hace que los datos estén disponibles en uno o varios formatos. En una transferencia del portapapeles, la aplicación llama a la función [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) para pasar un puntero de objeto de datos a OLE. (**OleSetClipboard** también ofrece formatos de datos de Portapapeles estándar para las aplicaciones OLE versión 1 y las que no son OLE). En una transferencia de arrastrar y colocar, la aplicación llama a la función [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) en su lugar.

En el lado receptor de la transferencia, el destino recibe el puntero [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) como argumento para una invocación de [**IDropTarget::D ROP**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) o llamando a la función [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) , dependiendo de si la transferencia es por medio de arrastrar y colocar o del portapapeles. Tras obtener este puntero, el destino llama a [**IDataObject:: del EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) para obtener información sobre los formatos que están disponibles para la recuperación y los tipos de medios que se pueden obtener. Con esta información, la aplicación receptora solicita los datos con una llamada a [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

