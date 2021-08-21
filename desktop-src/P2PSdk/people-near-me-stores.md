---
description: Equipos a mi alrededor Store
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Equipos a mi alrededor Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945a49d174f53037427aaa2f45dc0f567dc0acdba57e4a0b0231954e7e66fe90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061383"
---
# <a name="people-near-me-stores"></a>Equipos a mi alrededor Store

Las aplicaciones que [Equipos a mi alrededor](about-people-near-me.md) (PNM) pueden usar los siguientes almacenes de datos:

### <a name="windows-address-book"></a>Windows Libreta de direcciones

La Windows de direcciones almacena información sobre los contactos y sus certificados digitales. El contacto **"Me",** que representa el usuario que ha iniciado sesión actualmente, también se almacena en la Windows de direcciones.

### <a name="certificate-store"></a>Almacén de certificados

El almacén de certificados contiene el certificado autofirmado para el contacto **"Me".**

### <a name="application-store"></a>Tienda de aplicaciones

Un instalador de aplicaciones registra una aplicación con PNM durante el proceso de instalación. Estos son los objetos que otros usuarios pueden buscar al intentar conectarse a un usuario con una aplicación común, como un juego de equipo. Para cada aplicación, el Almacén de aplicaciones contiene el nombre de la aplicación, un identificador único global (GUID), un ámbito de la aplicación, una descripción y una ruta de acceso al archivo ejecutable del programa. El ámbito de una aplicación se puede establecer en Ninguno (no anunciado), Equipos a mi alrededor (anunciado en la subred local), Contactos (anunciado solo para contactos) o Todo (anunciado en la subred local y para contactos). El Almacén de aplicaciones se encuentra en el registro Windows Vista.

 

 



