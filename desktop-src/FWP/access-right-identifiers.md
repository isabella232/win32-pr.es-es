---
title: Identificadores de derecho de acceso (Fwpmu.h)
description: Windows La plataforma de filtrado (WFP) usa los derechos de acceso estándar de Win32 más un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado.
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
ms.openlocfilehash: 6deee82b792f525814ac4c841da8a848e4f7b978720755c82f93a9569ba21ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951384"
---
# <a name="access-right-identifiers"></a>Identificadores de derecho de acceso

Windows La plataforma de filtrado (WFP) usa los derechos de acceso estándar de [Win32](/windows/desktop/SecAuthZ/standard-access-rights) más un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado. Estos derechos de acceso solo se usan para proteger objetos en modo de usuario. Los llamadores en modo kernel omiten todas las comprobaciones de acceso.

Los identificadores de derecho de acceso específicos de WFP son los siguientes.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**
</dt> <dd> <dl> <dt>



Agregue un objeto al motor de filtrado base (BFE). Este derecho de acceso es necesario para llamar a las [**funciones Fwpm \* Add0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ ADD \_ LINK**
</dt> <dd> <dl> <dt>



Agregue un objeto al que se hace referencia a través de un vínculo. Por ejemplo, este derecho de acceso es necesario para las llamadas a las que se hace referencia a través de GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**
</dt> <dd> <dl> <dt>



Iniciar una transacción de solo lectura. Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**
</dt> <dd> <dl> <dt>



Iniciar una transacción de lectura y escritura. Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) para una transacción de lectura y escritura.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**
</dt> <dd> <dl> <dt>



Clasificar llamada a procedimiento remoto (RPC). El tiempo de ejecución de RPC necesita este derecho de acceso para aplicar filtros RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ ENUM**
</dt> <dd> <dl> <dt>



Enumerar. Este derecho de acceso es necesario para llamar a las funciones [**\* CreateEnumHandle0 de Fwpm.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) Para enumerar un objeto, el autor de la llamada también necesita acceso FWPM \_ ACTRL \_ READ al objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**
</dt> <dd> <dl> <dt>



Abra una sesión en el motor de filtros. Este derecho de acceso es necesario para llamar a [**FwpmEngineOpen0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**
</dt> <dd> <dl> <dt>



Lectura. Este derecho de acceso es necesario para llamar a las funciones [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) y [**Fwpm \* GetByKey0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**
</dt> <dd> <dl> <dt>



Leer estadísticas. Este derecho de acceso es necesario para llamar a [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IxtGetStatistics0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**
</dt> <dd> <dl> <dt>



Suscríbase. Este derecho de acceso es necesario para llamar a las funciones [**\* Fwpm SubscribeChanges0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) Para recibir una notificación de un objeto, un suscriptor también necesita acceso FWPM \_ ACTRL \_ READ al objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**
</dt> <dd> <dl> <dt>



Opciones del motor de escritura. Este derecho de acceso es necesario para llamar a [**FwpmEngineSetOption0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM \_ GENERIC \_ READ**
</dt> <dd> <dl> <dt>



DERECHOS \_ ESTÁNDAR READ \_ FWPM ACTRL BEGIN READ \| \_ \_ \_ \_ TXN \| FWPM \_ ACTRL \_ CLASSIFY \| FWPM \_ ACTRL OPEN \_ \| FWPM \_ ACTRL READ \_ \| FWPM ACTRL READ FWPM \_ ACTRL READ \_ \_ STATS


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>



DERECHOS \_ ESTÁNDAR \_ EXECUTE \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ SUBSCRIBE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**ESCRITURA GENÉRICA \_ FWPM \_**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ WRITE \| DELETE \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD \_ LINK \| FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ GENERIC \_ ALL**
</dt> <dd> <dl> <dt>



DERECHOS ESTÁNDAR REQUERIDOS \_ \_ \| FWPM \_ ACTRL ADD \_ \| FWPM \_ ACTRL \_ ADD LINK \_ FWPM ACTRL BEGIN READ \| \_ \_ \_ \_ TXN \| FWPM \_ ACTRL \_ BEGIN WRITE \_ \_ TXN \| FWPM \_ ACTRL CLASSIFY \_ \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL OPEN \_ \| FWPM \_ ACTRL READ \_ \| FWPM \_ ACTRL READ STATS \_ \_ \| FWPM \_ ACTRL SUBSCRIBE \_ FWPM ACTRL SUBSCRIBE \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Modelo de filtrado de Access Control plataforma](access-control.md)
</dt> <dt>

[Derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

