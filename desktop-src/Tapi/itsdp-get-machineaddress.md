---
description: El \_ método get MachineAddress obtiene la dirección de la máquina del host de origen.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Método ITSdp:: get_MachineAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690196"
---
# <a name="itsdpget_machineaddress-method"></a>ITSdp:: get \_ MachineAddress (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ MachineAddress** obtiene la dirección de la máquina del host de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMachineAddress* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene la dirección de la máquina del host de conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                        |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppMachineAddres* s no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                      |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppMachineAddress* .

El parámetro *ppMachineAddress* se puede devolver como un nombre DNS ("johnsmith.workinghard.Microsoft.com") o una dirección IP ("10.111.222.111").

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::p UT \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

