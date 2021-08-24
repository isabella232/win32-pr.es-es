---
title: Access Control (plataforma Windows filtrado de datos)
description: En Windows plataforma de filtrado de datos (WFP), el servicio Motor de filtrado base (BFE) implementa el modelo de control de acceso Windows estándar basado en tokens de acceso y descriptores de seguridad.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad8d1cc292358b156a8853a8a141426fda638d64474d1413747e2ebdb59d7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901105"
---
# <a name="access-control-windows-filtering-platform"></a>Access Control (plataforma Windows filtrado de datos)

En Windows plataforma de filtrado (WFP), el servicio Motor de filtrado base (BFE) implementa el modelo de [control](/windows/desktop/SecAuthZ/access-control-model) de acceso Windows estándar basado en tokens de acceso y descriptores de seguridad.

## <a name="access-control-model"></a>Access Control modelo

Se pueden especificar descriptores de seguridad al agregar nuevos objetos WFP, como filtros y subpestaciones. Los descriptores de seguridad se administran mediante las funciones de administración de WFP **Fwpm \* GetSecurityInfo0** y **Fwpm \* SetSecurityInfo0,** donde * _ representa el nombre del *\** objeto WFP. Estas funciones son semánticamente idénticas a las funciones Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) [**y SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

> [!Note]  
> No se puede llamar a las funciones **\* Fwpm SetSecurityInfo0** desde una transacción explícita.

 

> [!Note]  
> Las **funciones \* Fwpm SetSecurityInfo0** solo se pueden llamar desde una sesión dinámica si se usan para administrar un objeto dinámico creado dentro de la misma sesión.

 

El descriptor de seguridad predeterminado para el motor de filtro (el objeto engine raíz en el diagrama siguiente) es el siguiente.

-   Conceda derechos de acceso **\_ GENERIC ALL** (GA) al grupo de administradores integrado.
-   Conceda derechos de acceso GENERIC **\_ READ** (GR) **GENERIC \_ WRITE** (GW) **GENERIC \_ EXECUTE** (GX) a los operadores de configuración de red.
-   Conceda derechos de acceso **GRGWGX** a los siguientes identificadores de seguridad de servicio (SSID): MpsSvc (firewall de Windows), NapAgent (agente de protección de acceso de red), PolicyAgent (agente de directiva IPsec), RpcSs (llamada a procedimiento remoto) y WdiServiceHost (host de servicio de diagnóstico).
-   Conceda **FWPM \_ ACTRL \_ OPEN y** **FWPM \_ ACTRL \_ CLASSIFY** a todos los usuarios. (Estos son derechos de acceso específicos de WFP, que se describen en la tabla siguiente).

Los descriptores de seguridad predeterminados restantes se derivan a través de la herencia.

Hay algunas comprobaciones de acceso, como **para Fwpm \* Add0,** **Fwpm \* CreateEnumHandle0,** **Fwpm \* SubscribeChanges0,** que no se pueden realizar en el nivel de objeto individual. Para estas funciones, hay objetos de contenedor para cada tipo de objeto. Para los tipos de objeto estándar (por ejemplo, proveedores, llamadas, filtros), las funciones **Existentes \* GetSecurityInfo0** y **\* Fwpm SetSecurityInfo0** están sobrecargadas, de modo que un parámetro **GUID nulo** identifica el contenedor asociado. Para los demás tipos de objeto (por ejemplo, eventos de red y asociaciones de seguridad de IPsec), hay funciones explícitas para administrar la información de seguridad del contenedor.

BFE admite la herencia automática de entradas de control de acceso (ACE) Access Control lista de acceso discrecionales (DACL). BFE no admite AEE de Access Control sistema (SACL). Los objetos heredan las ACE de su contenedor. Los contenedores heredan las ACE del motor de filtro. Las rutas de propagación se muestran en el diagrama siguiente.

![Diagrama que muestra las rutas de propagación de ACE, empezando por "Motor".](images/access-control.jpg)

Para los tipos de objeto estándar, BFE aplica todos los derechos de acceso genéricos y estándar. Además, WFP define los siguientes derechos de acceso específicos.



| Derecho de acceso de WFP                                                                                                                        | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**<br/>                                       | Necesario para agregar un objeto a un contenedor.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ ADD \_ LINK**<br/>                       | Necesario para crear una asociación a un objeto . Por ejemplo, para agregar un filtro que haga referencia a una llamada, el autor de la llamada debe tener acceso ADD \_ LINK a la llamada.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**<br/>    | Necesario para iniciar una transacción de lectura explícita.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**<br/> | Necesario para iniciar una transacción de escritura explícita.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**<br/>                        | Necesario para clasificar en una capa de modo de usuario.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ ENUM**<br/>                                    | Necesario para enumerar los objetos de un contenedor. Sin embargo, el enumerador solo devuelve objetos a los que el autor de la llamada tiene acceso FWPM \_ ACTRL \_ READ.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**<br/>                                    | Necesario para abrir una sesión con BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**<br/>                                    | Necesario para leer las propiedades de un objeto.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**<br/>                 | Necesario para leer estadísticas.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**<br/>                     | Necesario para suscribirse a las notificaciones. Los suscriptores solo recibirán notificaciones para los objetos a los que tengan acceso FWPM \_ ACTRL \_ READ.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**<br/>                                 | Necesario para establecer las opciones del motor.<br/>                                                                                                                               |



 

BFE omite todas las comprobaciones de acceso para los llamadores en modo kernel.

Para evitar que los administradores se bloqueen a sí mismos fuera de BFE, a los miembros del grupo de administradores integrado siempre se les concede **FWPM \_ ACTRL \_ OPEN** al objeto de motor. Por lo tanto, un administrador puede recuperar el acceso mediante los pasos siguientes.

-   Habilite el **SE \_ TAKE OWNERSHIP \_ \_ NAME.**
-   Llame [**a FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La llamada se realiza correctamente porque el autor de la llamada es miembro de administradores integrados.
-   Tome posesión del objeto del motor. Esto se realiza correctamente porque el autor de la llamada **SE el privilegio TAKE OWNERSHIP \_ \_ \_ NAME.**
-   Actualice la DACL. Esto se realiza correctamente porque el propietario siempre tiene acceso **a \_ WRITE DAC.**

Dado que BFE admite su propia auditoría personalizada, no genera auditorías genéricas de acceso a objetos. Por lo tanto, se omite la SACL.

## <a name="wfp-required-access-rights"></a>Derechos de acceso requeridos de WFP

En la tabla siguiente se muestran los derechos de acceso necesarios para que las funciones de WFP accedan a varios objetos de la plataforma de filtrado. Las **funciones FwpmFilter \* *_ se muestran como un ejemplo para acceder a los objetos estándar. Todas las demás funciones que tienen acceso a objetos estándar siguen el modelo de* acceso de las funciones _ FwpmFilter. \***



Función

Objeto comprobado

Acceso requerido

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Motor

**FWPM \_ ACTRL \_ OPEN**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Motor

**FWPM \_ ACTRL \_ READ**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Motor

**FWPM \_ ACTRL \_ WRITE**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Motor

**FWPM \_ ACTRL \_ ENUM**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Motor

**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**  &  **FWPM \_ ACTRL BEGIN WRITE \_ \_ \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Proveedor de contenedores<br/> Nivel<br/> Sub-Layer<br/> Llamada<br/> Contexto del proveedor<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filter

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filter

**FWPM \_ ACTRL \_ READ**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtro de contenedor<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ READ**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Contenedor

**FWPM \_ ACTRL \_ SUBSCRIBE**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Contenedor

**FWPM \_ ACTRL \_ READ**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

Base de datos sa de IPsec

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

Base de datos sa de IPsec

**FWPM \_ ACTRL \_ ADD**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

Base de datos sa de IPsec

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

Base de datos sa de IPsec

**FWPM \_ ACTRL \_ READ**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

Base de datos sa de IPsec

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**IxtGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

Base de datos sa de IKE

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IxtSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

Base de datos sa de IKE

**DELETE**

[**IxtSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

Base de datos sa de IKE

**FWPM \_ ACTRL \_ READ**

[**IxtSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

Base de datos sa de IKE

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Contenedor

**FWPM \_ ACTRL \_ ENUM**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

No hay comprobaciones de acceso adicionales más allá de las de los filtros individuales y los contextos de proveedor.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Derechos de acceso estándar**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Windows de control de acceso](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows Filtrado de identificadores de derechos de acceso de plataforma**](access-right-identifiers.md)
</dt> </dl>

 

