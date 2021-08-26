---
title: Interfaces de transferencia de datos
description: Interfaces de transferencia de datos
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63bffa72f2e6bd408cbb7f19121aeef991e74702ff1141b24aba779e6985585c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896345"
---
# <a name="data-transfer-interfaces"></a>Interfaces de transferencia de datos

La [**interfaz IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) proporciona a los consumidores de datos métodos para obtener y establecer los datos de un objeto, determinar qué formatos admite el objeto y registrar y recibir notificaciones cuando cambian los datos del objeto. Al obtener datos, un autor de la llamada puede especificar el formato en el que desea representar los datos. Sin embargo, el origen de los datos determina el medio de almacenamiento, que devuelve en un parámetro out proporcionado por el autor de la llamada.

Por sí mismo, [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) proporciona todas las herramientas que necesita para implementar las Windows portapapeles o las transferencias de documentos compuestos en las aplicaciones. Si también desea admitir transferencias de arrastrar y colocar, debe implementar las interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) junto con **IDataObject**.

La [**interfaz IDataObject combinada**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) con las API del Portapapeles OLE proporciona todas las funcionalidades de Windows API del Portapapeles. Por lo general, no es necesario usar ambas API del Portapapeles. Los proveedores de datos que admiten transferencias de arrastrar y colocar o documentos compuestos OLE deben implementar la **interfaz IDataObject.** Si la aplicación solo admite ahora transferencias del Portapapeles, pero tiene previsto agregar documentos compuestos o de arrastrar y colocar en versiones posteriores, puede que quiera implementar **IDataObject** y las API del Portapapeles OLE ahora para minimizar la cantidad de tiempo invertido en la recuperación y depuración más adelante. Es posible que también quiera implementar **IDataObject para** usar medios de transferencia distintos de la memoria global.

En la tabla siguiente se resumen los que se usarán, en función de los tipos de transferencia de datos que quiera admitir:



| Para admitir                                                                       | Usar                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documentos compuestos<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Transferencias de arrastrar y colocar<br/>                                               | [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**IDropSource,**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) [**IDropTarget,**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (o el equivalente)<br/> |
| Transferencias del Portapapeles con memoria global exclusivamente<br/>                   | [API del Portapapeles](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Las transferencias del Portapapeles usan medios de intercambio distintos de la memoria global.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| El Portapapeles se transfiere ahora, pero arrastra y coloca documentos compuestos más adelante.<br/> | [**IDataObject y**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) las interfaces y la función enumeradas anteriormente para "Transferencias de arrastrar y colocar"<br/>                                                    |



 

Cuando un usuario inicia una operación de transferencia de datos, la aplicación de origen crea una instancia de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y, a través de ella, hace que los datos estén disponibles en uno o varios formatos. En una transferencia del Portapapeles, la aplicación llama a la [**función OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) para pasar un puntero de objeto de datos a OLE. (**OleSetClipboard también** ofrece formatos de datos estándar del Portapapeles para aplicaciones OLE versión 1 y no OLE). En una transferencia de arrastrar y colocar, la aplicación llama a la [**función DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) en su lugar.

En el lado receptor de la transferencia, el destino recibe el puntero [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) como argumento para una invocación de [**IDropTarget::D rop**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) o llamando a la función [**OleSetClipboard,**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) en función de si la transferencia se realiza mediante arrastrar y colocar o el Portapapeles. Una vez obtenido este puntero, el destino llama a [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) para obtener información sobre qué formatos están disponibles para la recuperación y sobre qué tipos de medios se pueden obtener. Con esta información, la aplicación receptora solicita los datos con una llamada a [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

