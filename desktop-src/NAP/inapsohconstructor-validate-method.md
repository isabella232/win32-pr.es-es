---
title: Método Validate de INapSoHConstructor (NapProtocol.h)
description: Comprueba la validez del paquete SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validación del método NAP
- Validación del método NAP, interfaz INapSoHConstructor
- INapSoHConstructor interface NAP , Validate (método)
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473760"
---
# <a name="inapsohconstructorvalidate-method"></a>INapSoHConstructor::Validate (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHConstructor::Validate** comprueba la validez del paquete SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*soh* \[ En\]
</dt> <dd>

Puntero al paquete [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) construido.

</dd> <dt>

*isRequest* \[ En\]
</dt> <dd>

Valor **BOOL** que es **TRUE** si el paquete es [**soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **FALSE** si es **soHResponse.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                  | El paquete SoH es válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**PAQUETE NAP \_ E \_ NO \_ VÁLIDO**</dt> </dl> | El paquete SoH no es válido.<br/>                              |



 

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





