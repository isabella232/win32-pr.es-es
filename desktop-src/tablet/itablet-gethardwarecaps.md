---
description: Devuelve un valor que representa las funciones del hardware de Tablet PC.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet:: GetHardwareCaps (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912341"
---
# <a name="itabletgethardwarecaps-method"></a>ITablet:: GetHardwareCaps (método)

Devuelve un valor que representa las funciones del hardware de Tablet PC.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwCaps* \[ enuncia\]
</dt> <dd>

Marcas de bits que representan las capacidades del hardware de Tablet PC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El parámetro *pdwCaps* es un conjunto de marcadores de bits que describen las capacidades de hardware de Tablet PC. En la tabla siguiente se describen estas marcas.



| Nombre de marca                         | Value                 | Descripción                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ integrado<br/>       | 0x00000001<br/> | Indica que la pantalla y el digitalizador comparten la misma superficie.<br/>                                                    |
| THWC \_ CSR \_ debe \_ tocar<br/> | 0x00000002<br/> | Indica que el cursor debe estar en contacto físico con el dispositivo para informar de la posición.<br/>                           |
| \_proximidad THWC \_<br/>  | 0x00000004<br/> | Indica que el dispositivo puede generar eventos cuando el cursor entra y sale del intervalo de detección física.<br/> |
| CSR de THWC \_ PHYSID \_<br/>     | 0x00000008<br/> | Indica que el dispositivo puede identificar de forma única el cursor activo en el hardware.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITablet**](itablet.md)
</dt> </dl>

 

 




