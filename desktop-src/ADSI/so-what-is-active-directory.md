---
title: Tutorial Overview ADSI with Visual Basic
description: Active Directory es una base de datos de uso especial \ 8212; no es un reemplazo del Registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cd6afe11b8991b6ced53367582ddf11d8eba0ea428105d3e9ba39c625d54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082259"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Introducción al tutorial: ADSI con Visual Basic

> [!Note]  
> La siguiente documentación forma parte de una descripción extendida del escenario para Visual Basic desarrolladores. Si busca información general sobre los Active Directory, consulte la documentación de [ti Pro sobre Technet.](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)) Para obtener una vista más detallada del lado de desarrollo de Active Directory, [vea Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Para obtener una introducción más amplia a Active Directory Service Interfaces, vea el tema primario de este tema: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), así como el tema relacionado: [About Active Directory Service Interfaces](about-adsi.md).

 

Active Directory es una base de datos de propósito especial, no es un reemplazo del Registro. El directorio está diseñado para controlar un gran número de operaciones de lectura y búsqueda y un número significativamente menor de cambios y actualizaciones. Active Directory datos son jerárquicos, replicados y extensibles. Dado que se replica, no quiere almacenar datos dinámicos, como los precios de las acciones corporativas o el rendimiento de la CPU. Si los datos son específicos de la máquina, almacene los datos en el Registro. Entre los ejemplos típicos de datos almacenados en el directorio se incluyen los datos de cola de impresora, los datos de contacto del usuario y los datos de configuración de red o equipo. La Active Directory base de datos consta de objetos y atributos. Los objetos y las definiciones de atributo se almacenan en Active Directory esquema.

Es posible que se pregunte qué objetos están almacenados actualmente en Active Directory. Active Directory tiene tres particiones. También se conocen como contextos de nomenclatura: dominio, esquema y configuración. La partición de dominio contiene usuarios, grupos, contactos, equipos, unidades organizativas y muchos otros tipos de objetos. Dado Active Directory es extensible, también puede agregar sus propias clases o atributos. La partición de esquema contiene clases y definiciones de atributos. La partición de configuración incluye datos de configuración para servicios, particiones y sitios.

En la siguiente captura de pantalla se muestra Active Directory partición de dominio.

![partición de dominio de Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso Active Directory mediante Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Escenario: Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 