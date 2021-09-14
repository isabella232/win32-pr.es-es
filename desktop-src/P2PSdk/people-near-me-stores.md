---
description: Equipos a mi alrededor store
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Equipos a mi alrededor store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244790"
---
# <a name="people-near-me-stores"></a>Equipos a mi alrededor store

Las aplicaciones que [Equipos a mi alrededor](about-people-near-me.md) (PNM) pueden usar los siguientes almacenes de datos:

### <a name="windows-address-book"></a>Windows Libreta de direcciones

La Windows de direcciones almacena información sobre los contactos y sus certificados digitales. El contacto **"Me",** que representa al usuario que ha iniciado sesión actualmente, también se almacena en la Windows de direcciones.

### <a name="certificate-store"></a>Almacén de certificados

El almacén de certificados contiene el certificado autofirmado para el contacto **"Me".**

### <a name="application-store"></a>Tienda de aplicaciones

Un instalador de aplicación registra una aplicación con PNM durante el proceso de instalación. Estos son los objetos que otros usuarios pueden buscar al intentar conectarse a un usuario con una aplicación común, como un juego de equipo. Para cada aplicación, el Almacén de aplicaciones contiene el nombre de la aplicación, un identificador único global (GUID), un ámbito de la aplicación, una descripción y una ruta de acceso al archivo ejecutable del programa. El ámbito de una aplicación se puede establecer en Ninguno (no anunciado), Equipos a mi alrededor (anunciado en la subred local), Contactos (anunciado solo para contactos) o Todo (anunciado en la subred local y para contactos). El Almacén de aplicaciones se encuentra en el registro Windows Vista.

 

 



