---
title: Interfaz INapComponentInfo (NapCommon.h)
description: Proporciona métodos que los componentes de complemento (como SHA y SHV) deben implementar para que el sistema NAP se comunique con ellos.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- NAP de la interfaz INapComponentInfo
- Interfaz NAP de INapComponentInfo , descrita
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188aae04ab407c5ae26e1d1a764e9093cc101cbe7d714ef8a8e0146013fefee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799710"
---
# <a name="inapcomponentinfo-interface"></a>INapComponentInfo (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapComponentInfo** proporciona métodos que los componentes del complemento (como SHA y SHV) deben implementar para que el sistema NAP se comunique con ellos. El sistema NAP llama a la implementación de estos métodos para recuperar información administrativa estática (por ejemplo, nombre descriptivo o cadenas localizadas).

## <a name="members"></a>Miembros

La **interfaz INapComponentInfo** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentInfo también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapComponentInfo** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Usado por el sistema NAP para solicitar al cliente de mantenimiento convertir un código de error HRESULT en un identificador de mensaje.<br/> |
| [**INapComponentInfo::GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Lo usa el sistema NAP para obtener la descripción de un cliente de mantenimiento.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Lo usa el sistema NAP para obtener el icono de un cliente de mantenimiento.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Lo usa el sistema NAP para obtener cadenas localizadas.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Lo usa el sistema NAP para obtener el nombre de proveedor de un cliente de mantenimiento.<br/>                                  |
| [**INapComponentInfo::GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

