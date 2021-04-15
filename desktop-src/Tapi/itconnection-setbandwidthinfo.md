---
description: El método SetBandwidthInfo establece la información de ancho de banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection:: SetBandwidthInfo (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690198"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>ITConnection:: SetBandwidthInfo (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetBandwidthInfo** establece la información de ancho de banda.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pModifier* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que indica el ámbito del ancho de banda que se establece. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> <dt>

*Ancho de banda* \[ de\]
</dt> <dd>

Consumo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pModifier* o *Bandwidth* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                     |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                    |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PModifier* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.

Referencia: RFC 2327.

Normalmente, el modificador de ancho de banda será CT o como:

**Total de la Conferencia CT:** Un ancho de banda máximo implícito se asocia a cada [*período*](t-tapgloss.md) de vida (TTL) en MBONE o en una región de ámbito administrativo de multidifusión determinada (las preguntas más frecuentes sobre el ancho de banda de MBONE en comparación con los límites de TTL). Si el ancho de banda de una sesión o un medio en una sesión es diferente del ancho de banda implícito del ámbito, a \` b = CT:... debe proporcionarse la línea para la sesión y proporcionar el límite superior propuesto al ancho de banda usado. El objetivo principal de esto es dar una idea aproximada de si dos o más conferencias pueden coexistir simultáneamente.

**Como Application-Specific máximo:** El ancho de banda se interpreta como específico de la aplicación, es decir, será el concepto de ancho de banda máximo de la aplicación. Normalmente, esto coincidirá con lo que se establece en el control de "ancho de banda máximo" de la aplicación, si procede.

Tenga en cuenta que CT proporciona una figura de ancho de banda total para todos los medios en todos los sitios. COMO proporciona una figura de ancho de banda para un solo medio en un único sitio, aunque puede haber muchos sitios que se envíen simultáneamente.

**Mecanismo de extensión:** Los escritores de herramientas pueden definir modificadores de ancho de banda experimental al prefijar los modificadores con "X-".

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

 

