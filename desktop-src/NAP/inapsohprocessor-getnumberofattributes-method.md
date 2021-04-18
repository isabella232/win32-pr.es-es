---
title: Método INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Recupera el número total de atributos del SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Método GetNumberOfAttributes NAP
- Método GetNumberOfAttributes NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534156"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a>INapSoHProcessor:: GetNumberOfAttributes (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHProcessor:: GetNumberOfAttributes** recupera el número total de atributos en el SOH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*attributeCount* \[ enuncia\]
</dt> <dd>

Puntero al número de atributos devueltos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





