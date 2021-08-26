---
description: El método \_ get MachineAddress obtiene la dirección del equipo del host de origen.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: Método ITSdp::get_MachineAddress (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e4d849c17d6c371a6edc927679e2ba6af344fbf8515310eb22b27ba4abeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012935"
---
# <a name="itsdpget_machineaddress-method"></a>ItSdp::get \_ MachineAddress (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ get MachineAddress** obtiene la dirección del equipo del host de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMachineAddress* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene la dirección del equipo del host de conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppMachineAddres* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                      |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppMachineAddress.*

El *parámetro ppMachineAddress* se puede devolver como un nombre DNS ("JohnSmith.workinghard.microsoft.com") o una dirección IP ("10.111.222.111").

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

