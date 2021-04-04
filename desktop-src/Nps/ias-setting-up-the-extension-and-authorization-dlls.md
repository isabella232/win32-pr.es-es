---
title: Configuración de los archivos dll de extensión
description: En el inicio, NPS comprueba el registro para obtener una lista de archivos dll de terceros a los que llamar.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078071"
---
# <a name="setting-up-the-extension-dlls"></a>Configuración de los archivos dll de extensión

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

En el inicio, NPS comprueba el registro para obtener una lista de archivos dll de terceros a los que llamar.

Para configurar una DLL de autenticación o de autorización en un servidor NPS, enumere las rutas de acceso a los archivos dll en valores inferiores a la siguiente clave del registro:

**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ Parameters\\**

Si no existen las claves **AuthSrv** y **Parameters** , créelos.

El valor en el que se enumeran los archivos dll de extensión de autenticación es:

**ExtensionDLLs**

El valor en el que se enumeran los archivos dll de la extensión de autorización es:

**AuthorizationDLLs**

Los valores **ExtensionDLLs** y **AuthorizationDLLs** deben ser de tipo **reg \_ multi \_ SZ**. Este tipo permite enumerar varios archivos dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Invocar los archivos dll de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 