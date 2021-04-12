---
title: Access Control (plataforma de filtrado de Windows)
description: En la plataforma de filtrado de Windows (WFP), el servicio motor de filtrado de base (BFE) implementa el modelo de control de acceso de Windows estándar basado en los tokens de acceso y los descriptores de seguridad.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104361796"
---
# <a name="access-control-windows-filtering-platform"></a>Access Control (plataforma de filtrado de Windows)

En la plataforma de filtrado de Windows (WFP), el servicio motor de filtrado de base (BFE) implementa el [modelo de control de acceso de Windows](/windows/desktop/SecAuthZ/access-control-model) estándar basado en los tokens de acceso y los descriptores de seguridad.

## <a name="access-control-model"></a>Modelo de Access Control

Los descriptores de seguridad se pueden especificar al agregar nuevos objetos de WFP, como filtros y subcapas. Los descriptores de seguridad se administran mediante las funciones de administración de WFP **Fwpm \* GetSecurityInfo0** y **Fwpm \* SetSecurityInfo0**, donde * *\** _ representa el nombre del objeto WFP. Estas funciones son semánticamente idénticas a las funciones de Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> No se puede llamar a las funciones **Fwpm \* SetSecurityInfo0** desde una transacción explícita.

 

> [!Note]  
> Solo se puede llamar a las funciones **Fwpm \* SetSecurityInfo0** desde una sesión dinámica si se usan para administrar un objeto dinámico creado dentro de la misma sesión.

 

El descriptor de seguridad predeterminado para el motor de filtro (el objeto de motor raíz en el diagrama siguiente) es el siguiente.

-   Conceda derechos de acceso **genéricos \_** (GA) al grupo de administradores integrado.
-   Conceda derechos de acceso genéricos de **\_ escritura** genérica de **\_ lectura** (de **GW) ( \_** GX) a los operadores de configuración de red.
-   Conceda derechos de acceso de **GRGWGX** a los siguientes identificadores de seguridad de servicio (SSID): MpsSvc (Firewall de Windows), NapAgent (agente de protección de acceso a redes), policyagent (agente de directivas IPSec), RPCSS (llamada a procedimiento remoto) y WdiServiceHost (host de servicio de diagnóstico).
-   Conceda **FWPM \_ ACTRL \_ Open** y **FWPM \_ ACTRL \_ clasificación** a todos los usuarios. (Estos son derechos de acceso específicos de WFP, que se describen en la tabla siguiente).

Los descriptores de seguridad predeterminados restantes se derivan a través de la herencia.

Hay algunas comprobaciones de acceso, como las llamadas de función **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , que no se pueden realizar en el nivel de objeto individual. Para estas funciones, hay objetos de contenedor para cada tipo de objeto. En el caso de los tipos de objeto estándar (por ejemplo, proveedores, llamadas, filtros), las funciones **Fwpm \* GetSecurityInfo0** y **Fwpm \* SetSecurityInfo0** existentes están sobrecargadas, de modo que un parámetro **GUID** null identifica el contenedor asociado. Para los demás tipos de objeto (por ejemplo, eventos de red y asociaciones de seguridad de IPsec), existen funciones explícitas para administrar la información de seguridad del contenedor.

BFE admite la herencia automática de entradas de control de acceso (ACE) de lista de Access Control discrecional (DACL). BFE no es compatible con las ACE de la lista de Access Control del sistema (SACL). Los objetos heredan las ACE de su contenedor. Los contenedores heredan las ACE del motor de filtro. Las rutas de propagación se muestran en el diagrama siguiente.

![Diagrama que muestra las rutas de propagación de ACE, comenzando por ' Engine '.](images/access-control.jpg)

En el caso de los tipos de objeto estándar, BFE aplica todos los derechos de acceso genéricos y estándar. Además, WFP define los siguientes derechos de acceso específicos.



| Derecho de acceso de WFP                                                                                                                        | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**<br/>                                       | Necesario para agregar un objeto a un contenedor.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ agregar \_ vínculo**<br/>                       | Necesario para crear una asociación con un objeto. Por ejemplo, para agregar un filtro que haga referencia a una llamada, el llamador debe tener \_ acceso de vínculo de adición a la llamada.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**<br/>    | Requerido para iniciar una transacción de lectura explícita.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**<br/> | Requerido para iniciar una transacción de escritura explícita.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_clasificación de ACTRL de FWPM \_**<br/>                        | Necesario para clasificar en una capa de modo de usuario.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL ( \_ enumeración)**<br/>                                    | Necesario para enumerar los objetos de un contenedor. Sin embargo, el enumerador solo devuelve los objetos a los que el autor de la llamada tiene acceso de lectura de FWPM \_ ACTRL \_ .<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**<br/>                                    | Necesario para abrir una sesión con BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lectura**<br/>                                    | Necesario para leer las propiedades de un objeto.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ leer \_ estadísticas**<br/>                 | Necesario para leer las estadísticas.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**suscripción a FWPM \_ ACTRL \_**<br/>                     | Necesario para suscribirse a las notificaciones. Los suscriptores solo recibirán notificaciones de los objetos a los que tengan acceso de lectura de FWPM \_ ACTRL \_ .<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**<br/>                                 | Necesario para establecer las opciones del motor.<br/>                                                                                                                               |



 

BFE omite todas las comprobaciones de acceso para los llamadores en modo kernel.

Para evitar que los administradores se bloqueen a través de BFE, los miembros del grupo de administradores integrados siempre reciben **FWPM \_ ACTRL \_ abierto** en el objeto Engine. Por lo tanto, un administrador puede recuperar el acceso a través de los pasos siguientes.

-   Habilite el **privilegio \_ usar \_ \_ nombre de propiedad** .
-   Llame a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La llamada se realiza correctamente porque el autor de la llamada es miembro de los administradores integrados.
-   Tomar posesión del objeto de motor. Esto se realiza correctamente porque el autor de la llamada tiene el privilegio de **\_ tomar \_ posesión del \_ nombre** .
-   Actualice la DACL. Esto se realiza correctamente porque el propietario siempre tiene acceso de **escritura de \_ DAC**

Dado que BFE admite su propia auditoría personalizada, no genera auditorías de acceso a objetos genéricos. Por lo tanto, se omite la SACL.

## <a name="wfp-required-access-rights"></a>Derechos de acceso de WFP requeridos

En la tabla siguiente se muestran los derechos de acceso requeridos por las funciones de WFP para tener acceso a varios objetos de plataforma de filtrado. Las **\* *funciones FwpmFilter _ se muestran como ejemplo de acceso a los objetos estándar. Todas las demás funciones que tienen acceso a objetos estándar siguen el modelo de acceso de* las funciones _ FwpmFilter \*** .



Función

Objeto comprobado

Acceso requerido

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Motor

**FWPM \_ ACTRL \_ Open**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Motor

**FWPM \_ ACTRL \_ lectura**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Motor

**FWPM \_ ACTRL \_ Write**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Motor

**FWPM \_ ACTRL ( \_ enumeración)**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Motor

**FWPM \_ ACTRL \_ Begin \_ lectura \_ TXN**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Proveedor de contenedores<br/> Nivel<br/> Sub-Layer<br/> Llamada<br/> Contexto de proveedor<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Add \_ Link**<br/> **FWPM \_ ACTRL \_ agregar \_ vínculo**<br/> **FWPM \_ ACTRL \_ agregar \_ vínculo**<br/> **FWPM \_ ACTRL \_ agregar \_ vínculo**<br/> **FWPM \_ ACTRL \_ agregar \_ vínculo**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filter

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filter

**FWPM \_ ACTRL \_ lectura**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtro de contenedor<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ lectura**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Contenedor

**suscripción a FWPM \_ ACTRL \_**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Contenedor

**FWPM \_ ACTRL \_ lectura**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

BD de IPsec SA

**FWPM \_ ACTRL \_ leer \_ estadísticas**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

BD de IPsec SA

**FWPM \_ ACTRL \_ Add**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

BD de IPsec SA

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

BD de IPsec SA

**FWPM \_ ACTRL \_ lectura**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

BD de IPsec SA

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

BD DE IKE SA

**FWPM \_ ACTRL \_ leer \_ estadísticas**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

BD DE IKE SA

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

BD DE IKE SA

**FWPM \_ ACTRL \_ lectura**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

BD DE IKE SA

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Contenedor

**FWPM \_ ACTRL ( \_ enumeración)**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Ninguna comprobación de acceso adicional más allá de las de los filtros y contextos de proveedor individuales



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Derechos de acceso estándar**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modelo de control de acceso de Windows](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Identificadores de derechos de acceso de la plataforma de filtrado de Windows**](access-right-identifiers.md)
</dt> </dl>

 

