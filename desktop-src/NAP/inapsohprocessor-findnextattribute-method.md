---
title: Método INapSoHProcessor FindNextAttribute (NapProtocol.h)
description: Busca la ubicación (índice) del siguiente atributo del tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Método NAP de FindNextAttribute
- Método NAP de FindNextAttribute, interfaz INapSoHProcessor
- INapSoHProcessor interface NAP , FindNextAttribute method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071672"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>INapSoHProcessor::FindNextAttribute (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSoHProcessor::FindNextAttribute** busca la ubicación (índice) del atributo siguiente del tipo indicado por *SoHAttributeType*.

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

*fromLocation* \[ En\]
</dt> <dd>

Ubicación inicial (índice) del paquete Statement of Health (SoH) para iniciar la búsqueda de atributos. Este valor debe estar en el intervalo de 0 a (**numAttrib** - 1) donde **numAttrib** se recupera mediante [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> El paquete SoH usa índices de atributo basados en 0.

 

</dd> <dt>

*type* \[ En\]
</dt> <dd>

Estructura [**SoHAttributeType**](sohattributetype-enum.md) que contiene el tipo de atributo que se debe buscar.

</dd> <dt>

*attributeLocation* \[ out\]
</dt> <dd>

Puntero que contiene la ubicación (índice) en el paquete SoH del primer atributo de tipo *SoHAttributeType* del índice *fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**</dt> </dl> | No se encontró el atributo.<br/>                                    |



 

## <a name="remarks"></a>Observaciones

El **método FindNextAttribute** busca atributos de tipo *SoHAttributeType* del índice especificado por *fromLocation* y superiores hasta que se encuentra una coincidencia. Si no se encuentra ninguna coincidencia, **se devuelve ERROR FILE NOT \_ \_ \_ FOUND.**

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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





