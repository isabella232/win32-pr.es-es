---
title: Interfaz INapComponentInfo (NapCommon. h)
description: Proporciona métodos que los componentes de complemento (como Sha y SHV) deben implementar para que el sistema NAP se comunique con ellos.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Interfaz INapComponentInfo NAP
- Interfaz INapComponentInfo NAP, descripción
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
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996184"
---
# <a name="inapcomponentinfo-interface"></a>Interfaz INapComponentInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapComponentInfo** proporciona métodos que los componentes de complemento (como Sha y SHV) deben implementar para que el sistema NAP se comunique con ellos. El sistema NAP llama a la implementación de estos métodos para recuperar información administrativa estática (por ejemplo, un nombre descriptivo o cadenas localizadas).

## <a name="members"></a>Miembros

La interfaz **INapComponentInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapComponentInfo** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Lo usa el sistema NAP para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un ID. de mensaje.<br/> |
| [**INapComponentInfo:: GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Lo usa el sistema NAP para obtener la descripción de un cliente de mantenimiento.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.<br/>                                |
| [**INapComponentInfo:: GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Lo usa el sistema NAP para obtener el icono de un cliente de mantenimiento.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Lo usa el sistema NAP para obtener cadenas traducidas.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Lo usa el sistema NAP para obtener el nombre del proveedor de un cliente de mantenimiento.<br/>                                  |
| [**INapComponentInfo:: GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

