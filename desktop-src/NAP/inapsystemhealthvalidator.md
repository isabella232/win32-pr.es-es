---
title: Interfaz INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deben ser implementados por los desarrolladores de SHV para permitir que el sistema NAP se comunique con un SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Interfaz INapSystemHealthValidator NAP
- Interfaz INapSystemHealthValidator NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801826"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interfaz INapSystemHealthValidator

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthValidator** proporciona métodos que los desarrolladores de SHV deben implementar para permitir que el sistema NAP se comunique con un SHV.

## <a name="members"></a>Miembros

La interfaz **INapSystemHealthValidator** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSystemHealthValidator** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator:: Validate**](inapsystemhealthvalidator-validate-method.md) | El sistema NAP llama a este método definido por la aplicación para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

