---
description: En esta sección se describe la estructura de calidad de servicio (QOS) específica del protocolo para ATM, que se encuentra en el campo ProviderSpecific de la estructura de QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensión QoS de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154240"
---
# <a name="winsock-atm-qos-extension"></a>Extensión QoS de ATM de Winsock

En esta sección se describe la estructura de calidad de servicio ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) específica del protocolo para ATM, que se encuentra en el campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) de la estructura de **QoS** . Tenga en cuenta que el uso de esta estructura **QoS** específica de ATM es opcional para los clientes de Windows Sockets 2, y el proveedor de servicios ATM es necesario para asignar la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) genérica a los elementos de información Q. 2931 adecuados. Sin embargo, si se especifican tanto la estructura **FLOWSPEC** genérica como la estructura de **QoS** específica de ATM, el valor especificado en la estructura **QoS** específica de ATM debería tener prioridad en caso de que se produzcan conflictos. Consulte la sección 2,7 de la especificación de la API de Windows Sockets 2 para obtener más información sobre las provisiones de QoS y la estructura **FLOWSPEC** .

La estructura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica del protocolo para ATM es una concatenación de estructuras Q. 2931 Information Element (IE), que se definen en el siguiente texto. Si una aplicación omite un e/o que el UNI 3. x asigna, el proveedor de servicios debe insertar un valor predeterminado razonable, teniendo en cuenta la información de la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) si es aplicable.

La administración de s repetida depende del propio IE. Si se repite una IE y es una que se puede repetir según la especificación UNI del Foro de ATM, el proveedor debe administrarla correctamente. En este caso, el orden de la lista determina el orden de las preferencias, con los elementos que aparecen anteriormente en la lista que son más preferidos. Si se repite una instancia de IE y esto no se permite por especificación UNI del Foro de ATM, el proveedor puede producir un error en la solicitud del cliente (la opción preferida) o usar el último IE de ese tipo encontrado.

Cada estructura individual de IE tiene el formato de la siguiente manera y se identifica mediante el campo **IEType** :

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Los valores válidos para el campo **IEType** se definen como:

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

El campo de **IE** está superpuesto por una estructura específica de IE y el campo **IELength** es la longitud total en bytes de la estructura de IE, incluidos los campos **IEType** y **IELength** . La semántica y los valores válidos para cada elemento de estas estructuras de Internet Explorer son por cada especificación UNI 3. x de ATM. \_El campo \_ de SAP ausente se puede usar para los elementos que son opcionales para una estructura de IE determinada, según la especificación de UNI 3. x de ATM.

 

 
