---
description: Tiendas de equipos a mi alrededor
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Tiendas de equipos a mi alrededor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911313"
---
# <a name="people-near-me-stores"></a>Tiendas de equipos a mi alrededor

Las aplicaciones capaces de usar equipos a [mi alrededor](about-people-near-me.md) (PNM) pueden utilizar los siguientes almacenes de datos:

### <a name="windows-address-book"></a>Libreta de direcciones de Windows

La libreta de direcciones de Windows almacena información sobre los contactos y sus certificados digitales. El contacto "**me**", que representa el usuario que ha iniciado la sesión, también se almacena en la libreta de direcciones de Windows.

### <a name="certificate-store"></a>Almacén de certificados

El almacén de certificados contiene el certificado autofirmado para el contacto "**me**".

### <a name="application-store"></a>Tienda de aplicaciones

Un instalador de aplicaciones registra una aplicación con PNM durante el proceso de instalación. Estos son los objetos que pueden buscar otros usuarios al intentar conectarse a un usuario con una aplicación común, como un juego de equipos. Para cada aplicación, el almacén de aplicaciones contiene el nombre de la aplicación, un identificador único global (GUID), un ámbito de la aplicación, una descripción y una ruta de acceso al archivo ejecutable del programa. El ámbito de una aplicación se puede establecer en ninguno (no anunciado), equipos a mi alrededor (anunciado en la subred local), contactos (anunciados solo para contactos) o todo (anunciado en la subred local y para contactos). El almacén de aplicaciones se encuentra en el registro de Windows Vista.

 

 



