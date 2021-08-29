---
description: El método get BandwidthModifier obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que da el significado de \_ la figura de ancho de banda. Los dos modificadores definidos son CT (total de conferencias) y AS (máximo específico de la aplicación).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: Método ITConnection::get_BandwidthModifier (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4624ee0dce757f3e7d94327ad52e4c45f57f364c6e1e6286d183b50ff15243d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406155"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a>ItConnection::get \_ BandwidthModifier (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ BandwidthModifier** obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que da el significado de la figura de ancho de banda. Los dos modificadores definidos son CT (total de conferencias) y AS (máximo específico de la aplicación).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppModifier* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene el modificador de ancho de banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppModifier* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppModifier.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

