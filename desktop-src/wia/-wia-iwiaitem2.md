---
description: La interfaz IWiaItem2 proporciona a las aplicaciones la misma funcionalidad que la interfaz IWiaItem (la capacidad de consultar dispositivos para detectar sus funcionalidades, acceder a interfaces de transferencia de datos y propiedades de elementos y controlar el dispositivo).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: Interfaz IWiaItem2 (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573153"
---
# <a name="iwiaitem2-interface"></a>Interfaz IWiaItem2

La **interfaz IWiaItem2** proporciona a las aplicaciones la misma funcionalidad que la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacidad de consultar dispositivos para detectar sus funcionalidades, acceder a interfaces de transferencia de datos y propiedades de elementos y controlar el dispositivo). También proporciona a la aplicación la capacidad de crear y usar dinámicamente filtros de procesamiento de imágenes que pueden ser extensiones de los controladores de dispositivo de adquisición de imágenes (WIA) 2.0 de Windows proporcionados en Windows Vista.

## <a name="members"></a>Members

La **interfaz IWiaItem2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaItem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaItem2** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | Comprueba si una extensión especificada está disponible en la máquina y la puede usar el [**método IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md) <br/>                                   |
| [**CreateChildItem**](-wia-iwiaitem2-createchilditem.md)               | Cree un nuevo elemento secundario. Agrega **objetos IWiaItem2** al árbol **IWiaItem2** de un dispositivo. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Quita el objeto **IWiaItem2** actual del árbol de objetos del dispositivo. <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | Emite un comando a un dispositivo de hardware WIA 2.0. <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | Muestra un cuadro de diálogo al usuario para prepararse para la adquisición de imágenes. <br/>                                                                                                                              |
| [**Diagnóstico**](-wia-iwiaitem2-diagnostic.md)                         | No se admite actualmente.<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | Crea un objeto enumerador y devuelve un puntero a su [**interfaz IEnumWiaItem2**](-wia-ienumwiaitem2.md) para carpetas con elementos en el árbol **IWiaItem2** de un dispositivo WIA 2.0. <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo WIA 2.0. <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | El [**método IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) crea un enumerador que se usa para obtener información sobre los eventos para los que se registra una aplicación.<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | Busca en el árbol de subelementos de un elemento con el nombre como clave de búsqueda. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Obtiene las interfaces de extensión que pueden ir con un controlador de dispositivo WIA 2.0. <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | Obtiene la información de categoría de un elemento. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Obtiene la información de tipo de un elemento. <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | Obtiene el elemento primario del árbol que representa un dispositivo de hardware WIA 2.0. <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Obtiene el componente de versión preliminar de WIA 2.0.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware WIA 2.0. <br/>                                                                                                        |



 

## <a name="remarks"></a>Observaciones

El árbol de elementos de WIA 2.0 que puede ver una aplicación es independiente del árbol creado y mantenido por un minidriver de WIA 2.0. Cuando un minidriver crea un árbol de elementos, el servicio WIA 2.0 usa este árbol de elementos de WIA 2.0 como guía para crear copias idénticas que las aplicaciones de creación de imágenes pueden ver. Los elementos del árbol copiado se denominan elementos de aplicación. Los elementos del árbol creado por un minidriver se denominan elementos de controlador. En Windows Vista, los árboles de elementos de WIA 2.0 se construyen con objetos **IWiaItem2,** cada uno de los cuales implementa la **interfaz IWiaItem2).**

La **interfaz IWiaItem2,** al igual que todas las interfaces del Modelo de objetos componentes (COM), hereda los métodos [de interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
