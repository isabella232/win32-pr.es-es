---
description: El \_ método get BandwidthModifier obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que ofrece el significado de la figura de ancho de banda. Los dos modificadores definidos son CT (total de la Conferencia) y como (máximo específico de la aplicación).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Método ITConnection:: get_BandwidthModifier (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679324"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a>ITConnection:: get \_ BandwidthModifier (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ BandwidthModifier** obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que ofrece el significado de la figura de ancho de banda. Los dos modificadores definidos son CT (total de la Conferencia) y como (máximo específico de la aplicación).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppModifier* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene el modificador de ancho de banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppModifier* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppModifier* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

