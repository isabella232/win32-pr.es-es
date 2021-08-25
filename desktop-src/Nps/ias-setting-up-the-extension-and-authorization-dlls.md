---
title: Configuración de los archivos DLL de extensión
description: Al iniciarse, NPS busca en el Registro una lista de archivos DLL de terceros a los que llamar.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962515"
---
# <a name="setting-up-the-extension-dlls"></a>Configuración de los archivos DLL de extensión

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

Al iniciarse, NPS busca en el Registro una lista de archivos DLL de terceros a los que llamar.

Para configurar un archivo DLL de autenticación o autorización en un servidor NPS, enumé una lista de las rutas de acceso a los archivos DLL en valores debajo de la siguiente clave del Registro:

**Parámetros \\ \\ \\ \\ AuthSrv del sistema HKLM CurrentControlSet Services \\\\**

Si las **claves AuthSrv** y **Parameters** no existen, cándalas.

El valor en el que se enumeran los archivos DLL de extensión de autenticación es:

**ExtensionDLLs**

El valor en el que se enumeran los archivos DLL de la extensión de autorización es:

**AuthorizationDLLs**

Los valores **ExtensionDLLs** y **AuthorizationDLLs** deben ser de tipo **REG MULTI \_ \_ SZ**. Este tipo le permite enumerar varios archivos DLL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Invocación de los archivos DLL de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 