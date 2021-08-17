---
title: Interfaz INapClientManagement2 (NapManagement.h)
description: Proporciona métodos para la administración de clientes NAP. | Interfaz INapClientManagement2 (NapManagement.h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- NAP de interfaz INapClientManagement2
- Nap de interfaz INapClientManagement2 , descrito
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f459e6fa0d883203bf52ebbd0aaab06ee93cef00d1fb52af3d670f71cf7ab52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800105"
---
# <a name="inapclientmanagement2-interface"></a>Interfaz INapClientManagement2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapClientManagement2** proporciona métodos para la administración de clientes NAP.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapClientManagement**](inapclientmanagement.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapClientManagement2** hereda de [**INapClientManagement**](inapclientmanagement.md). **INapClientManagement2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapClientManagement2** tiene estos métodos.



| Método                                                                                                    | Descripción                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Recupera información sobre el estado de aislamiento y el estado de aislamiento extendido del cliente nap.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





