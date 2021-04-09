---
description: El método ManageChannel crea un comando de unidad de datos de protocolo de aplicación (APDU) que abre y cierra los canales lógicos.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816:: ManageChannel (método) (Scardssp. h)'
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
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082456"
---
# <a name="iscardiso7816managechannel-method"></a>ISCardISO7816:: ManageChannel (método)

\[El método **ManageChannel** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ManageChannel** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que abre y cierra los canales lógicos.

La función Open abre un nuevo canal lógico distinto del básico. Se proporcionan opciones para que la tarjeta asigne un número de canal lógico, o para el número de canal lógico que se va a proporcionar a la tarjeta.

La función Close cierra explícitamente un canal lógico que no sea el básico. Después del cierre correcto, el canal lógico estará disponible para su reutilización.

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

*byChannelState* \[ de\]
</dt> <dd>

El bit B8 de P1 se usa para indicar la función Open o la función Close; Si B8 es 0, el canal de administración debe abrir un canal lógico y, si B8 es 1, el canal de administración debe cerrar un canal lógico:

P1 = ' 00 ' para abrir

P1 = ' 80 ' para cerrar

Otros valores son RFU

</dd> <dt>

*byChannel* \[ de\]
</dt> <dd>

En el caso de la función Open (P1 = ' 00 '), los bits B1 y B2 de P2 se usan para codificar el número de canal lógico de la misma manera que en el byte de la clase, los otros bits de P2 son RFU.

Cuando B1 y B2 de P2 son **null**, la tarjeta asignará un número de canal lógico que se devolverá en los bits B1 y B2 del campo de datos.

Cuando B1 y/o B2 de P2 no son **null**, codifican un número de canal lógico distinto del básico; a continuación, la tarjeta abrirá el número de canal lógico asignado externamente.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Cuando la función Open se realiza correctamente desde el canal lógico básico, el MF se seleccionará implícitamente como el DF actual y el estado de seguridad del nuevo canal lógico debe ser el mismo que el canal lógico básico después de ATR. El estado de seguridad del nuevo canal lógico debe ser independiente del de cualquier otro canal lógico.

Cuando la función Open se realiza correctamente desde un canal lógico, que no es la básica, el DF actual del canal lógico que emitió el comando se seleccionará como el DF actual. Además, el estado de seguridad del nuevo canal lógico debe ser el mismo que el estado de seguridad del canal lógico desde el que se realizó la función abierta.

Después de una función de cierre correcta, se pierde el estado de seguridad relacionado con este canal lógico.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
