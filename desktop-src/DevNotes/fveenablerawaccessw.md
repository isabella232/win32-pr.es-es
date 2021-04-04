---
description: Habilita o deshabilita la lectura y escritura de sectores de disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW función)
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
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907117"
---
# <a name="fveenablerawaccessw-function"></a>FveEnableRawAccessW función)

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

*VolumeName* \[ de\]
</dt> <dd>

Un identificador único para el volumen de disco.

</dd> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Si **es true**, permite el acceso al volumen sin formato. Si es **false**, no se permite el acceso al volumen sin procesar. Si ya se ha habilitado el acceso sin procesar, pero este valor es **false**, el volumen se vuelve a montar y a validar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                           | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                           | La función se realizó correctamente.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Enabled es **false** y el volumen no estaba ya en modo de acceso sin procesar.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | No se puede bloquear el volumen.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




