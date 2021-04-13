---
title: Información general del tutorial ADSI con Visual Basic
description: Active Directory es una base de datos de uso especial \ 8212; no es un reemplazo del registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104559779"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Información general del tutorial: ADSI con Visual Basic

> [!Note]  
> La siguiente documentación es parte de una descripción del escenario extendido para los desarrolladores de Visual Basic. Si está buscando una introducción general de Active Directory, consulte los [documentos de profesionales de TI en TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Para obtener una visión más detallada del lado de desarrollo de Active Directory, vea [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Para obtener una introducción más grande a las interfaces de servicio de Active Directory, vea el tema principal de este tema: Active Directory de las [interfaces de servicio](active-directory-service-interfaces-adsi.md), así como el tema relacionado: [acerca de las interfaces de servicio de Active Directory](about-adsi.md).

 

Active Directory es una base de datos Especial, no es un reemplazo del registro. El directorio está diseñado para controlar un gran número de operaciones de lectura y búsqueda y un número significativamente menor de cambios y actualizaciones. Active Directory datos son jerárquicos, replicados y extensibles. Dado que se replica, no desea almacenar los datos dinámicos, como los precios de las acciones corporativas o el rendimiento de la CPU. Si los datos son específicos de la máquina, almacene los datos en el registro. Algunos ejemplos típicos de los datos almacenados en el directorio son los datos de la cola de impresión, los datos de contacto de usuario y los datos de configuración de red o equipo. La base de datos Active Directory consta de objetos y atributos. Los objetos y las definiciones de atributo se almacenan en el esquema de Active Directory.

Es posible que se pregunte qué objetos están almacenados actualmente en Active Directory. Active Directory tiene tres particiones. También se conocen como contextos de nomenclatura: dominio, esquema y configuración. La partición de dominio contiene usuarios, grupos, contactos, equipos, unidades organizativas y muchos otros tipos de objetos. Dado que Active Directory es extensible, también puede agregar sus propios atributos y clases. La partición del esquema contiene clases y definiciones de atributos. La partición de configuración incluye datos de configuración de servicios, particiones y sitios.

En la captura de pantalla siguiente se muestra la Active Directory partición de dominio.

![partición de dominio de Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a Active Directory mediante Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Escenario: fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 