---
title: Inicialización del Protocolo de autenticación
description: La conexión segura EAP se inicializa entre el cliente y el servidor de maneras similares para los clientes RAS e inalámbrico (802.1 X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856bd173ef617fb272460f874fa1d2087322c8b4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420622"
---
# <a name="authentication-protocol-initialization"></a>Inicialización del Protocolo de autenticación

La conexión segura EAP se inicializa entre el cliente y el servidor de maneras similares para los clientes RAS e inalámbrico (802.1 X).

## <a name="client"></a>Remoto

Cuando el cliente intenta establecer la conexión, el servicio de autenticación obtiene la [información de identidad](obtaining-identity-information.md) del usuario. Si el valor NAMEDLG de la **\_ \_ \_ \_ invocación del ValueName EAP de Ras** está presente en el registro para este protocolo de autenticación y este valor se establece en cero, el servicio de autenticación llama a [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Normalmente, esta función muestra una interfaz de usuario que permite que la información de identidad sea de un tipo específico del Protocolo de autenticación; por ejemplo, un certificado o un identificador numérico. Si **la \_ \_ \_ invocación de \_ NAMEDLG de EAP de Ras** no está presente o se establece en uno, el servicio de autenticación muestra el cuadro de diálogo de nombre de usuario estándar del sistema.

Una vez que el servicio de autenticación ha obtenido la información de identidad del usuario, llama a la implementación del Protocolo de autenticación de [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Esta llamada permite al Protocolo de autenticación asignar e inicializar un búfer de trabajo que el servicio pasa en llamadas posteriores a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) y [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)). El búfer de trabajo es opaco para el servicio y nunca tiene acceso al contenido del búfer de trabajo. Si el protocolo de autenticación crea un búfer de trabajo distinto para cada sesión EAP, el búfer de trabajo es sesión y seguro para subprocesos. Dado que el protocolo de autenticación asigna la memoria para el búfer de trabajo, el protocolo de autenticación también debe liberar esta memoria mediante la función [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) .

En la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), el servicio también pasa una estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contiene punteros a la información de configuración para la conexión y la información de identidad del usuario. El servicio siempre pasa un valor para el miembro **pszIdentity** de **\_ \_ entrada EAP de PPP**. Sin embargo, el miembro **pszPassword** de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) puede ser **null**.

Dentro de la estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) , el miembro **fAuthenticator** indica si se está invocando el protocolo de autenticación para autenticarse (en el cliente) o como el autenticador (en el servidor).

## <a name="server"></a>Servidor

En el servidor, el miembro **bInitialID** de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) especifica el identificador que utiliza el servidor para el primer paquete EAP. El servidor incrementa este identificador para los paquetes posteriores.

Además, en el servidor, el puntero **pUserAttributes** de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) apunta a una matriz de atributos del tipo de [**\_ \_ atributo \_ de autenticación ras**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) . Estos son los atributos del usuario que se obtuvieron del cliente.

Si la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) devuelve un valor distinto **de \_ error**, la sesión se desconecta. El error devuelto se registra (en el servidor) o se muestra al usuario (en el cliente).

 

 