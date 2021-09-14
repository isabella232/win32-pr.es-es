---
title: Interfaz INapSystemHealthValidator (NapSystemHealthValidator.h)
description: Los desarrolladores de SHV deben implementarlo para permitir que el sistema NAP se comunique con una SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP de la interfaz INapSystemHealthValidator
- Interfaz NAP de INapSystemHealthValidator , descrita
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161272"
---
# <a name="inapsystemhealthvalidator-interface"></a>INapSystemHealthValidator (interfaz)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSystemHealthValidator proporciona** métodos que deben implementar los desarrolladores de SHV para permitir que el sistema NAP se comunique con una SHV.

## <a name="members"></a>Members

La **interfaz INapSystemHealthValidator** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSystemHealthValidator** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator::Validate**](inapsystemhealthvalidator-validate-method.md) | El sistema NAP llama a este método definido por la aplicación para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

