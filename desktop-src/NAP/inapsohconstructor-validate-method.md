---
title: Método Validate de INapSoHConstructor (NapProtocol. h)
description: Comprueba la validez del paquete SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validar el método NAP
- Método Validate NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método Validate
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803104"
---
# <a name="inapsohconstructorvalidate-method"></a>INapSoHConstructor:: Validate (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHConstructor:: Validate** comprueba la validez del paquete SOH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SOH* \[ de de\]
</dt> <dd>

Puntero al paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) construido.

</dd> <dt>

*isRequest* \[ de\]
</dt> <dd>

Valor **booleano** que es **true** si el paquete es un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si es un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                  | El paquete SoH es válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**\_paquete NAP E \_ no válido \_**</dt> </dl> | El paquete SoH no es válido.<br/>                              |



 

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





