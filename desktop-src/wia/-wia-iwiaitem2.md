---
description: La interfaz IWiaItem2 proporciona a las aplicaciones la misma funcionalidad que la interfaz IWiaItem (la capacidad de consultar dispositivos para detectar sus capacidades, tener acceso a las interfaces de transferencia de datos y las propiedades de los elementos, y para controlar el dispositivo).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: Interfaz IWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908005"
---
# <a name="iwiaitem2-interface"></a>Interfaz IWiaItem2

La interfaz **IWiaItem2** proporciona a las aplicaciones la misma funcionalidad que la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacidad de consultar dispositivos para detectar sus capacidades, tener acceso a las interfaces de transferencia de datos y las propiedades de los elementos, y para controlar el dispositivo). También proporciona a las aplicaciones la capacidad de crear y usar de forma dinámica filtros de procesamiento de imágenes que pueden ser extensiones de los controladores de dispositivos de adquisición de imágenes de Windows (WIA) 2,0 proporcionados en Windows Vista.

## <a name="members"></a>Miembros

La interfaz **IWiaItem2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaItem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaItem2** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | Comprueba si una extensión especificada está disponible en el equipo y puede ser utilizada por el método [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) . <br/>                                   |
| [**CreateChildItem**](-wia-iwiaitem2-createchilditem.md)               | Cree un nuevo elemento secundario. Agrega objetos **IWiaItem2** al árbol **IWiaItem2** de un dispositivo. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Quita el objeto **IWiaItem2** actual del árbol de objetos del dispositivo. <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | Emite un comando para un dispositivo de hardware WIA 2,0. <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | Muestra un cuadro de diálogo al usuario para preparar la adquisición de imágenes. <br/>                                                                                                                              |
| [**Diagnóstico**](-wia-iwiaitem2-diagnostic.md)                         | No se admite actualmente.<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | Crea un objeto de enumerador y devuelve un puntero a su interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para carpetas con elementos en el árbol **IWiaItem2** de un dispositivo WIA 2,0. <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo WIA 2,0. <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | El método [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) crea un enumerador que se usa para obtener información sobre los eventos para los que se registra una aplicación.<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | Busca en el árbol de subelementos de un elemento utilizando el nombre como clave de búsqueda. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Obtiene las interfaces de extensión que pueden presentarse con un controlador de dispositivo WIA 2,0. <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | Obtiene la información de la categoría de un elemento. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Obtiene la información de tipo de un elemento. <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | Obtiene el elemento primario del árbol que representa un dispositivo de hardware WIA 2,0. <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Obtiene el componente de vista previa de WIA 2,0.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware WIA 2,0. <br/>                                                                                                        |



 

## <a name="remarks"></a>Observaciones

El árbol de elementos de WIA 2,0 que puede ver una aplicación es independiente del árbol que crea y mantiene un minicontrolador de WIA 2,0. Cuando un minicontrolador crea un árbol de elementos, el servicio WIA 2,0 usa este árbol de elementos de WIA 2,0 como guía para crear copias idénticas que puedan ver las aplicaciones de creación de imágenes. Los elementos del árbol copiado se denominan elementos de la aplicación. Los elementos del árbol creados por un minicontrolador se denominan elementos de controlador. En Windows Vista, los árboles de elementos de WIA 2,0 se compilan de objetos **IWiaItem2** , cada uno de los cuales implementa la interfaz **IWiaItem2** ).

La interfaz **IWiaItem2** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
