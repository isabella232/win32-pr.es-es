---
title: Acceder a los identificadores de derechos (Fwpmu. h)
description: La plataforma de filtrado de Windows (WFP) usa los derechos de acceso estándar de Win32 junto con un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997063"
---
# <a name="access-right-identifiers"></a>Acceder a los identificadores de derechos

La plataforma de filtrado de Windows (WFP) usa los [derechos de acceso estándar de Win32](/windows/desktop/SecAuthZ/standard-access-rights) junto con un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado. Estos derechos de acceso se usan para proteger objetos solo en modo de usuario. Los llamadores de modo kernel omiten todas las comprobaciones de acceso.

Los identificadores de derechos de acceso específicos de WFP son los siguientes.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**
</dt> <dd> <dl> <dt>



Agregue un objeto al motor de filtrado de base (BFE). Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ agregar \_ vínculo**
</dt> <dd> <dl> <dt>



Agregue un objeto al que se hace referencia a través de un vínculo. Por ejemplo, este derecho de acceso es necesario para las llamadas a las que se hace referencia a través de GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**
</dt> <dd> <dl> <dt>



Comienza una transacción de solo lectura. Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**
</dt> <dd> <dl> <dt>



Comienza una transacción de lectura/escritura. Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) para una transacción de lectura/escritura.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_clasificación de ACTRL de FWPM \_**
</dt> <dd> <dl> <dt>



Clasifique llamada a procedimiento remoto (RPC). Este derecho de acceso es necesario para el tiempo de ejecución de RPC con el fin de aplicar los filtros RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL ( \_ enumeración)**
</dt> <dd> <dl> <dt>



Enumerar. Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) . Para enumerar un objeto, el llamador también necesita el \_ acceso de lectura de FWPM ACTRL \_ al objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**
</dt> <dd> <dl> <dt>



Abra una sesión en el motor de filtro. Este derecho de acceso es necesario para llamar a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lectura**
</dt> <dd> <dl> <dt>



Lectura. Este derecho de acceso es necesario para llamar a las funciones [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) y [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ leer \_ estadísticas**
</dt> <dd> <dl> <dt>



Leer estadísticas. Este derecho de acceso es necesario para llamar a [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) y [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**suscripción a FWPM \_ ACTRL \_**
</dt> <dd> <dl> <dt>



Suscríbase. Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) . Para recibir una notificación de un objeto, un suscriptor también necesita \_ el acceso de lectura de FWPM ACTRL \_ al objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**
</dt> <dd> <dl> <dt>



Opciones del motor de escritura. Este derecho de acceso es necesario para llamar a [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lectura genérica \_ FWPM**
</dt> <dd> <dl> <dt>



STANDARD \_ Rights \_ Read \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN \| FWPM \_ ACTRL \_ clasifique \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_ejecución genérica de FWPM \_**
</dt> <dd> <dl> <dt>



\_derechos estándar \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ subscribe


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_escritura genérica de FWPM \_**
</dt> <dd> <dl> <dt>



STANDARD \_ Rights \_ Write \| Delete \| FWPM \_ ACTRL \_ agregar \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ Write


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ genérico \_ todo**
</dt> <dd> <dl> <dt>



\_derechos estándar \_ obligatorios \| FWPM \_ ACTRL \_ agregar \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN FWPM \| \_ ACTRL \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ clasifique \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats \| FWPM ACTRL \_ \_ subscribe FWPM ACTRL \| \_ \_ Write


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de Access Control de plataforma de filtrado de Windows](access-control.md)
</dt> <dt>

[Derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

