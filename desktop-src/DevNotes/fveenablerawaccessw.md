---
description: Habilita o deshabilita la lectura y escritura de sectores de disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Función FveEnableRawAccessW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956094"
---
# <a name="fveenablerawaccessw-function"></a>Función FveEnableRawAccessW

Habilita o deshabilita la lectura y escritura de sectores de disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeName* \[ En\]
</dt> <dd>

Identificador único para el volumen de disco.

</dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Si **es TRUE,** permite el acceso al volumen sin formato. Si **es FALSE,** no se permite el acceso al volumen sin formato. Si ya se ha habilitado el acceso sin procesar pero este valor es **FALSE,** el volumen se vuelve a montar y se vuelve a validar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                           | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                           | La función se ha realizado correctamente.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Habilitado es **FALSE** y el volumen aún no estaba en modo de acceso sin formato.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | El volumen no se puede bloquear.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




