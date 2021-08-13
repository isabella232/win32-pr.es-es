---
description: El método ManageChannel crea un comando de unidad de datos de protocolo de aplicación (APDU) que abre y cierra los canales lógicos.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: Método ISCardISO7816::ManageChannel (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92fb91c0630996938e247dbc244ac0c311c52531401367d5326bd197ffaabf9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481132"
---
# <a name="iscardiso7816managechannel-method"></a>Método ISCardISO7816::ManageChannel

\[El **método ManageChannel** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método ManageChannel** crea un comando de unidad de datos [*de*](../secgloss/a-gly.md) protocolo de aplicación (APDU) que abre y cierra los canales lógicos.

La función open abre un nuevo canal lógico distinto del básico. Se proporcionan opciones para que la tarjeta asigne un número de canal lógico o para que el número de canal lógico se suministre a la tarjeta.

La función close cierra explícitamente un canal lógico distinto del básico. Después del cierre correcto, el canal lógico estará disponible para volver a usarse.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byChannelState* \[ En\]
</dt> <dd>

El bit b8 de P1 se usa para indicar la función open o la función close; Si b8 es 0, MANAGE CHANNEL abrirá un canal lógico y, si b8 es 1, MANAGE CHANNEL cerrará un canal lógico:

P1 = '00' para abrir

P1 = '80' para cerrar

Otros valores son RFU

</dd> <dt>

*byChannel* \[ En\]
</dt> <dd>

Para la función open (P1 = '00'), los bits b1 y b2 de P2 se usan para codificar el número de canal lógico de la misma manera que en el byte de clase, los demás bits de P2 son RFU.

Cuando b1 y b2 de P2 son **NULL,** la tarjeta asignará un número de canal lógico que se devolverá en los bits b1 y b2 del campo de datos.

Cuando b1 y/o b2 de P2 no son **NULL,** codifican un número de canal lógico distinto del básico; a continuación, la tarjeta abrirá el número de canal lógico asignado externamente.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **NULL.**

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Cuando la función abierta se realiza correctamente desde el canal lógico básico, la MF se seleccionará implícitamente como el DF actual y el estado de seguridad del nuevo canal lógico debe ser el mismo que el canal lógico básico después de ATR. El estado de seguridad del nuevo canal lógico debe ser independiente del de cualquier otro canal lógico.

Cuando la función open se realiza correctamente desde un canal lógico, que no es el básico, el DF actual del canal lógico que emitió el comando se seleccionará como el DF actual. Además, el estado de seguridad del nuevo canal lógico debe ser el mismo que el del canal lógico desde el que se realizó la función abierta.

Después de una función de cierre correcta, se pierde el estado de seguridad relacionado con este canal lógico.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
