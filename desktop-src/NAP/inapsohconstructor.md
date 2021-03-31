---
title: Interfaz INapSoHConstructor (NapProtocol. h)
description: Los Sha usan para construir SoHRequests y SHV para construir SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Interfaz INapSoHConstructor NAP
- Interfaz INapSoHConstructor NAP, descripción
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995993"
---
# <a name="inapsohconstructor-interface"></a>Interfaz INapSoHConstructor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSoHConstructor** proporciona métodos que los Sha usan para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) y SHV para construir **SoHResponses**.

## <a name="members"></a>Miembros

La interfaz **INapSoHConstructor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHConstructor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSoHConstructor** tiene estos métodos.



| Método                                                                                   | Descripción                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Agrega un TLV al final del búfer de SoH.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Recupera el paquete SoH construido.<br/>    |
| [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md)           | Inicializa el paquete SoH.<br/>              |
| [**INapSoHConstructor:: Validate**](inapsohconstructor-validate-method.md)               | Comprueba la validez del paquete SoH.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

