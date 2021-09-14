---
description: El método SetBandwidthInfo establece la información de ancho de banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: Método ITConnection::SetBandwidthInfo (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068744"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>ItConnection::SetBandwidthInfo (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetBandwidthInfo** establece la información de ancho de banda.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pModifier* \[ En\]
</dt> <dd>

Puntero a un **BSTR que** indica el ámbito del ancho de banda que se va a establecer. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> <dt>

*Ancho de banda* \[ En\]
</dt> <dd>

Banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pModifier* *o Bandwidth* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                     |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                    |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pModifier* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

Referencia: RFC 2327.

Normalmente, el modificador de ancho de banda será CT o AS:

**Total de conferencias de CT:** Se asocia un ancho [](t-tapgloss.md) de banda máximo implícito a cada período de vida (TTL) en Mional o dentro de una región de ámbito administrativo de multidifusión determinada (el ancho de banda de Mhz frente a los límites de TTL se dan en las preguntas más frecuentes de MBone). Si el ancho de banda de una sesión o un medio de una sesión es diferente del ancho de banda implícito del ámbito, \` b=CT:...' line debe proporcionarse para la sesión, lo que proporciona el límite superior propuesto al ancho de banda utilizado. El propósito principal de esto es dar una idea aproximada de si dos o más conferencias pueden coexistir simultáneamente.

**As Application-Specific máximo:** El ancho de banda se interpreta como específico de la aplicación, es decir, será el concepto de ancho de banda máximo de la aplicación. Normalmente, esto coincidirá con lo que se establece en el control "ancho de banda máximo" de la aplicación, si procede.

Tenga en cuenta que CT proporciona una cifra de ancho de banda total para todos los medios en todos los sitios. AS proporciona una figura de ancho de banda para un único medio en un único sitio, aunque puede haber muchos sitios enviando simultáneamente.

**Mecanismo de extensión:** Los escritores de herramientas pueden definir modificadores de ancho de banda experimentales antefiriendo sus modificadores con "X-".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

