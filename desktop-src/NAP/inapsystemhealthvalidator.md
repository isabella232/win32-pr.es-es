---
title: Interfaz INapSystemHealthValidator (NapSystemHealthValidator.h)
description: Los desarrolladores de SHV deben implementarlo para permitir que el sistema NAP se comunique con una SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP de la interfaz INapSystemHealthValidator
- Nap de interfaz INapSystemHealthValidator , descrito
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
ms.openlocfilehash: 7310afe1c61dd61344bd1ed355f78735dc7785f9016bbcbb702073b2a06feba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686065"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interfaz INapSystemHealthValidator

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthValidator proporciona** métodos que los desarrolladores de SHV deben implementar para permitir que el sistema NAP se comunique con una SHV.

## <a name="members"></a>Miembros

La **interfaz INapSystemHealthValidator** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthValidator** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator::Validate**](inapsystemhealthvalidator-validate-method.md) | El sistema NAP llama a este método definido por la aplicación para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

