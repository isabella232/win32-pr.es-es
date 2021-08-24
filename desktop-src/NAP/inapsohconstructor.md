---
title: Interfaz INapSoHConstructor (NapProtocol.h)
description: Las SHA usan para construir SoHRequests y shvs para construir SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- NAP de interfaz INapSoHConstructor
- Interfaz NAP de INapSoHConstructor , descrito
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceb9e927e1ac65f21a3ff457922e1bd475b8327ac2525b2af7afefa6cb173f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037856"
---
# <a name="inapsohconstructor-interface"></a>Interfaz INapSoHConstructor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **INapSoHConstructor** proporciona métodos que usan los SHA para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) y los SHV para construir **SoHResponses.**

## <a name="members"></a>Miembros

La **interfaz INapSoHConstructor** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHConstructor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSoHConstructor** tiene estos métodos.



| Método                                                                                   | Descripción                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Agrega un TLV al final del búfer soH.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Recupera el paquete SoH construido.<br/>    |
| [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md)           | Inicializa el paquete SoH.<br/>              |
| [**INapSoHConstructor::Validate**](inapsohconstructor-validate-method.md)               | Comprueba la validez del paquete SoH.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

