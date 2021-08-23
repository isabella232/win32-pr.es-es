---
title: Inicialización del protocolo de autenticación
description: La conexión segura de EAP se inicializa entre el cliente y el servidor de maneras similares para clientes RAS e inalámbricos (802.1X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984465"
---
# <a name="authentication-protocol-initialization"></a>Inicialización del protocolo de autenticación

La conexión segura de EAP se inicializa entre el cliente y el servidor de maneras similares para clientes RAS e inalámbricos (802.1X).

## <a name="client"></a>Cliente

Cuando el cliente intenta establecer la conexión, el servicio de autenticación obtiene información [de identidad](obtaining-identity-information.md) del usuario. Si el **valor \_ DE EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** de RAS está presente en el Registro para este protocolo de autenticación y este valor se establece en cero, el servicio de autenticación llama a [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Esta función normalmente muestra una interfaz de usuario que permite que la información de identidad sea de un tipo específico del protocolo de autenticación; por ejemplo, un certificado o un identificador numérico. Si **RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** no está presente o está establecido en uno, el servicio de autenticación muestra el cuadro de diálogo nombre de usuario del sistema estándar.

Una vez que el servicio de autenticación ha obtenido la información de identidad del usuario, llama a la implementación del protocolo de autenticación de [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Esta llamada permite al protocolo de autenticación asignar e inicializar un búfer de trabajo que el servicio pasa en llamadas posteriores a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) y [**RasEapEnd.**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) El búfer de trabajo es opaco para el servicio y nunca tiene acceso al contenido del búfer de trabajo. Si el protocolo de autenticación crea un búfer de trabajo distinto para cada sesión eap, el búfer de trabajo es seguro para la sesión y el subproceso. Dado que el protocolo de autenticación asigna la memoria para el búfer de trabajo, el protocolo de autenticación también debe liberar esta memoria mediante la [**función RasEapFreeMemory.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

En la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), el servicio también pasa una estructura [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contiene punteros a la información de configuración de la conexión y la información de identidad del usuario. El servicio siempre pasa un valor para el **miembro pszIdentity** de **PPP EAP \_ \_ INPUT**. Sin embargo, el **miembro pszPassword** de [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) puede ser **NULL.**

Dentro de la estructura [**\_ PPP EAP \_ INPUT,**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) el miembro **fAuthenticator** indica si se invoca el protocolo de autenticación para autenticarse (en el cliente) o como autenticador (en el servidor).

## <a name="server"></a>Servidor

En el servidor, el **miembro bInitialID** de [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) especifica el identificador que el servidor usa para el primer paquete EAP. El servidor incrementa este identificador para los paquetes posteriores.

También en el servidor, el puntero **pUserAttributes** en [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) apunta a una matriz de atributos del tipo RAS [**\_ AUTH ATTRIBUTE \_ \_ TYPE.**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) Estos son atributos para el usuario que se han obtenido del cliente.

Si la [**llamada a RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) devuelve cualquier valor distinto de **NO \_ ERROR**, la sesión se desconecta. El error devuelto se registra (en el servidor) o se muestra al usuario (en el cliente).

 

 