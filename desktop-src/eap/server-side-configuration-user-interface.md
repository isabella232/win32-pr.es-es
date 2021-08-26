---
title: Server-Side configuración Interfaz de usuario
description: Implemente una interfaz de usuario de configuración para el servidor mediante la implementación de la interfaz COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92bf6a1f5b5f0e1302e68dd8ca9070771bfbc7714759a384f67782ffdad6e2ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021815"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side configuración Interfaz de usuario

Implemente una interfaz de usuario de configuración para el servidor mediante la implementación de la interfaz [**COM, IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Esta interfaz COM se deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y agrega tres métodos: [**IEAPProviderConfig::Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig::ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)e [**IEAPProviderConfig::Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

La interfaz de usuario debe admitir la administración remota. En otras palabras, aunque la interfaz de usuario configurará el protocolo de autenticación en el servidor, la propia interfaz de usuario puede estar ejecutándose en otro equipo. Para admitir la administración remota, separe el código de la interfaz de usuario del código que realmente realiza la configuración. El código de configuración reside en el servidor en el que se ejecuta el protocolo de autenticación.

Use el Active Template Library (ATL) para implementar [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Para más información, consulte la interfaz de usuario de configuración del lado servidor de ejemplo en el directorio de ejemplos del SDK. El identificador de clase (CLSID) para el objeto de interfaz de usuario de configuración debe colocarse en el Registro con un nombre de valor de [RAS \_ EAP \_ VALUENAME CONFIG \_ \_ CLSID](authentication-protocol-registry-values.md). Para obtener más información, vea [Valores del Registro del protocolo de autenticación](authentication-protocol-registry-values.md).

Cuando el usuario hace clic en el botón Configurar para un protocolo de autenticación en el cuadro de diálogo Propiedades de Enrutamiento y RAS, el sistema comprueba si existe un valor \_ DE \_ \_ CLSID DE CONFIGURACIÓN DE EAP DE RAS VALUENAME para este protocolo de autenticación en el \_ Registro. Si es así, COM crea una instancia del objeto de interfaz de usuario de configuración. Si el sistema no encuentra RAS EAP VALUENAME CONFIG CLSID en el Registro y el sistema tiene acceso a Servicios de directorio \_ \_ \_ (DS), el sistema intenta crear una instancia del objeto desde el Almacén de \_ clases.

En el caso de que el usuario esté conectado a varias máquinas simultáneamente, se crea una instancia de varios objetos de interfaz de usuario de configuración.

 

 