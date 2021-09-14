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
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071676"
---
# <a name="inapsohconstructor-interface"></a>Interfaz INapSoHConstructor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **INapSoHConstructor** proporciona métodos que usan los SHA para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) y los SHV para construir **SoHResponses.**

## <a name="members"></a>Members

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
| Encabezado<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

