---
title: Método INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Busca la ubicación (índice) del siguiente atributo del tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Método FindNextAttribute NAP
- Método FindNextAttribute NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801316"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>INapSoHProcessor:: FindNextAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSoHProcessor:: FindNextAttribute** busca la ubicación (índice) del siguiente atributo del tipo indicado por *SoHAttributeType*.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fromLocation* \[ de\]
</dt> <dd>

La ubicación inicial (índice) en el paquete del informe de mantenimiento (SoH) para comenzar la búsqueda de atributos. Este valor debe estar en el intervalo de 0 a (**numAttrib** -1), donde **numAttrib** se recupera mediante [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> El paquete SoH utiliza índices de atributos basados en 0.

 

</dd> <dt>

*tipo* \[ de de\]
</dt> <dd>

Estructura [**SoHAttributeType**](sohattributetype-enum.md) que contiene el tipo de atributo que se va a buscar.

</dd> <dt>

*attributeLocation* \[ enuncia\]
</dt> <dd>

Un puntero que contiene la ubicación (índice) en el paquete SoH del primer atributo de tipo *SoHAttributeType* del índice *fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo de error**</dt> </dl> | No se encontró el atributo.<br/>                                    |



 

## <a name="remarks"></a>Observaciones

El método **FindNextAttribute** busca atributos de tipo *SoHAttributeType* desde el índice especificado por *fromLocation* y superior hasta que se encuentre una coincidencia. Si no se encuentra ninguna coincidencia, se devuelve el **archivo de error \_ \_ no \_ encontrado** .

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

 

 





