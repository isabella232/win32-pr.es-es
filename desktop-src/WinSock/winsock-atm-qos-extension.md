---
description: En esta sección se describe la estructura de calidad de servicio (QOS) específica del protocolo para ATM, que se encuentra en el campo ProviderSpecific de la estructura QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensión QoS de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612825"
---
# <a name="winsock-atm-qos-extension"></a>Extensión QoS de ATM de Winsock

En esta sección se describe la estructura de calidad de servicio [**(QOS)**](/windows/win32/api/winsock2/ns-winsock2-qos)específica del protocolo para ATM, que se encuentra en el campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) de la **estructura QOS.** Tenga en cuenta que el uso de esta estructura **QOS** específica de ATM es opcional para los clientes de Windows Sockets 2 y el proveedor de servicios DE ATM es necesario para asignar la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) genérica a los elementos de información de Q.2931 adecuados. Sin embargo, si se especifican tanto la estructura **FLOWSPEC** genérica como la estructura QOS específica de **ATM,** el valor especificado en la estructura **QOS** específica de ATM debe tener prioridad en caso de que haya conflictos. Consulte Windows especificación de API de Sockets 2 sección 2.7 para obtener más información sobre las aprovisionaciones de QoS y **la estructura FLOWSPEC.**

La estructura [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica del protocolo para ATM es una concatenación de estructuras de elementos de información (IE) de Q.2931, que se definen en el texto siguiente. Si una aplicación omite un IE que uni 3.x exige, el proveedor de servicios debe insertar un valor predeterminado razonable, teniendo en cuenta la información de la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) si procede.

El control de las E/S repetidas depende del propio IE. Si se repite un IE y se permite que se repita según la especificación DE UNIDAD del foro de ATM, el proveedor debe controlarlo correctamente. En este caso, el orden de la lista determina el orden de preferencias, y los elementos que aparecen anteriormente en la lista son más preferidos. Si se repite un IE y esto no se permite según la especificación UNI del foro de ATM, el proveedor puede producir un error en la solicitud del cliente (la opción preferida) o usar el último IE de ese tipo encontrado.

Cada estructura de IE individual tiene el formato siguiente y se identifica mediante el **campo IEType:**

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Los valores legales del **campo IEType** se definen como:

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

El **campo IE** está superado por una estructura de IE específica y el campo **IELength** es la longitud total en bytes de la estructura de IE, incluidos los campos **IEType** **e IELength.** La semántica y los valores legales de cada elemento de estas estructuras de IE se encuentran según la especificación DE UNI 3.x de ATM. SAP FIELD ABSENT se puede usar para los elementos que son opcionales para una estructura de IE determinada, según la especificación \_ \_ UNI 3.x de ATM.

 

 
