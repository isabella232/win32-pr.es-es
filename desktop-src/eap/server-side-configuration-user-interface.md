---
title: Interfaz de usuario de configuración de Server-Side
description: Implemente una interfaz de usuario de configuración para el servidor implementando la interfaz COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0904c90fea2bef3ccc00c00135be09a711d8454
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358918"
---
# <a name="server-side-configuration-user-interface"></a>Interfaz de usuario de configuración de Server-Side

Implemente una interfaz de usuario de configuración para el servidor implementando la interfaz COM, [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Esta interfaz COM deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y agrega tres métodos: [**IEAPProviderConfig:: Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig:: ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)y [**IEAPProviderConfig:: UnInitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

La interfaz de usuario debe admitir la administración remota. En otras palabras, aunque la interfaz de usuario configurará el protocolo de autenticación en el servidor, la propia interfaz de usuario se puede estar ejecutando en un equipo diferente. Para admitir la administración remota, separe el código de la interfaz de usuario del código que realmente realiza la configuración. El código de configuración reside en el servidor en el que se ejecuta el protocolo de autenticación.

Use el Active Template Library (ATL) para implementar [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Para obtener más información, consulte la interfaz de usuario de configuración del servidor de ejemplo en el directorio de ejemplos del SDK. El identificador de clase (CLSID) para el objeto de interfaz de usuario de configuración debe colocarse en el registro con un nombre de valor de [ras \_ EAP \_ ValueName \_ config \_ CLSID](authentication-protocol-registry-values.md). Para obtener más información, vea [valores del registro del Protocolo de autenticación](authentication-protocol-registry-values.md).

Cuando el usuario hace clic en el botón configurar de un protocolo de autenticación en el cuadro de diálogo Propiedades para el enrutamiento y el RAS, el sistema comprueba si \_ \_ existe un \_ valor CLSID para el protocolo de autenticación EAP de Ras \_ en el registro. Si es así, COM crea instancias del objeto de la interfaz de usuario de configuración. Si el sistema no puede encontrar RAS \_ EAP \_ ValueName \_ config \_ CLSID en el registro y el sistema tiene acceso a los servicios de directorio (DS), el sistema intenta crear una instancia del objeto desde el almacén de clases.

En el caso en el que el usuario está conectado a varios equipos simultáneamente, se crean instancias de varios objetos de interfaz de usuario de configuración.

 

 