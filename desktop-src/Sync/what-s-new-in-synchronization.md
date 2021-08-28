---
description: Windows incluye los siguientes nuevos elementos de programación para la sincronización.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Novedades de la sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e998e4c925fdfc702e0a54ec9fce53ab24577c97f563670fc1710dd1308a21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959063"
---
# <a name="whats-new-in-synchronization"></a>Novedades de la sincronización

Windows incluye los siguientes nuevos elementos de programación para la sincronización.

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>Funciones nuevas

<dl> <dt>

[**DeleteSynchronizationBarrona**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

Elimina una barrera de sincronización.

</dd> <dt>

[**EnterSynchronizationBarrona**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Hace que el subproceso que realiza la llamada espere en una barrera de sincronización hasta que el número máximo de subprocesos haya entrado en la barrera.

</dd> <dt>

[**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

Recupera los resultados de una operación superpuesta en el archivo, canalización con nombre o dispositivo de comunicaciones especificados dentro del intervalo de tiempo de espera especificado. El subproceso que realiza la llamada puede realizar una espera que se puede alertar.

</dd> <dt>

[**InitializeSynchronizationBarrona**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Especifica el número máximo de subprocesos y número de número de subprocesos para una nueva barrera de sincronización.

</dd> <dt>

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

Espera a que cambie el valor de la dirección especificada.

</dd> <dt>

[**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

Reactiva todos los subprocesos que esperan a que cambie el valor de una dirección.

</dd> <dt>

[**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

Reactiva un subproceso que está esperando a que cambie el valor de una dirección.

</dd> </dl>

### <a name="new-interlocked-functions"></a>Nuevas funciones entrelazados

<dl> <dt>

[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

Realiza una operación de suma atómica en los valores **LONG** especificados. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

Realiza una operación de suma atómica en los valores **LONGLONG** especificados. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

Realiza una operación AND atómica en los valores **LONG especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

Realiza una operación AND atómica en los valores **char especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

Realiza una operación AND atómica en los valores **SHORT especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

Realiza una operación AND atómica en los valores **LONGLONG especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

Prueba el bit especificado del valor **LONG64** especificado y lo complementa. La operación es atómica.

</dd> <dt>

[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

Prueba el bit especificado del valor **LONG** especificado y lo establece en 0. La operación es atómica y se realiza con la semántica de adquisición de ordenación de memoria.

</dd> <dt>

[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

Prueba el bit especificado del valor **LONG** especificado y lo establece en 0. La operación es atómica y se realiza mediante la semántica de liberación de memoria.

</dd> <dt>

[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

Comprueba el bit especificado del valor **LONG** especificado y lo establece en 1. La operación es atómica y se realiza con la semántica de adquisición de ordenación de memoria.

</dd> <dt>

[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

Comprueba el bit especificado del valor **LONG** especificado y lo establece en 1. La operación es atómica y se realiza con semántica de ordenación de memoria de versión.

</dd> <dt>

[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 32 bits especificados e intercambia con otro valor de 32 bits en función del resultado de la comparación. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 16 bits especificados e intercambia con otro valor de 16 bits en función del resultado de la comparación.

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 16 bits especificados e intercambia con otro valor de 16 bits en función del resultado de la comparación. La operación se realiza con la semántica de adquisición de ordenación de memoria.

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 16 bits especificados e intercambia con otro valor de 16 bits en función del resultado de la comparación. El intercambio se realiza con semántica de ordenación de memoria de versión.

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 16 bits especificados e intercambia con otro valor de 16 bits en función del resultado de la comparación. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 64 bits especificados e intercambia con otro valor de 64 bits en función del resultado de la comparación. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de 128 bits especificados e intercambia con otro valor de 128 bits en función del resultado de la comparación.

</dd> <dt>

[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

Realiza una operación atómica de comparación e intercambio en los valores especificados. La función compara dos valores de puntero especificados e intercambia con otro valor de puntero en función del resultado de la comparación. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 32 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica.

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza con la semántica de adquisición de ordenación de memoria.

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza con semántica de ordenación de memoria de versión.

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

Disminuye (disminuye en uno) el valor de la variable de 64 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

Establece una variable de 64 bits en el valor especificado como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

Establece una variable de 8 bits en el valor especificado como una operación atómica.

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

Establece una variable de 16 bits en el valor especificado como una operación atómica. La operación se realiza mediante la adquisición de semántica de ordenación de memoria.

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

Establece una variable de 16 bits en el valor especificado como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

Establece una variable de 64 bits en el valor especificado como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

Intercambia de forma atómica un par de direcciones. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

Realiza una adición atómica de dos valores de 32 bits. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

Realiza una adición atómica de dos valores de 64 bits. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 32 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica.

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza mediante la adquisición de semántica de ordenación de memoria.

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza mediante la semántica de ordenación de memoria de versión.

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

Incrementa (aumenta en uno) el valor de la variable de 64 bits especificada como una operación atómica. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

Realiza una operación OR atómica en los valores **LONG** especificados. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

Realiza una operación OR atómica en los valores **char especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

Realiza una operación OR atómica en los valores **SHORT especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

Realiza una operación OR atómica en los valores **LONGLONG especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

Inserta una lista vinculada de forma singly al frente de otra lista vinculada de forma singly. El acceso a las listas se sincroniza en un sistema de varios procesadores. Esta versión del método no usa la convención [ \_ \_ de llamada rápida.](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx)

</dd> <dt>

[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

Realiza una operación XOR atómica en los valores **LONG** especificados. La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

Realiza una operación XOR atómica en los valores **char especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

Realiza una operación XOR atómica en los valores **SHORT especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

Realiza una operación XOR atómica en los valores **LONGLONG especificados.** La operación se realiza de forma atómica, pero sin usar barreras de memoria.

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>Funciones nuevas

<dl> <dt>

[**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

Activa el temporizador de espera especificado y proporciona información de contexto para el temporizador.

</dd> <dt>

[**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

Intenta adquirir un bloqueo lector/escritor (SRW) más fino en modo exclusivo. Si la llamada se realiza correctamente, el subproceso de llamada toma posesión del bloqueo.

</dd> <dt>

[**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

Intenta adquirir un bloqueo lector/escritor (SRW) más fino en modo compartido. Si la llamada se realiza correctamente, el subproceso de llamada toma posesión del bloqueo.

</dd> </dl>

### <a name="new-structures"></a>Nuevas estructuras

<dl> <dt>

[**CONTEXTO DE \_ MOTIVO**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

Contiene información de contexto para un temporizador activado [**con SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).

</dd> </dl>

 

 
