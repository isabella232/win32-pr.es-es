---
description: El Windows puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159167"
---
# <a name="advertisement"></a>Anuncio

El Windows puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación. Si se anuncia una aplicación, solo se presentan al usuario u otras aplicaciones las interfaces necesarias para cargar e iniciar la aplicación. Si un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios como se describe en [Instalación a petición.](installation-on-demand.md)

Los dos tipos de publicidad son asignación y publicación. Aparece una aplicación instalada para un usuario cuando esa aplicación se asigna al usuario. El **menú** Inicio contiene los accesos directos adecuados, se muestran iconos, los archivos están asociados a la aplicación y las entradas del Registro reflejan la instalación de la aplicación. Cuando el usuario intenta abrir una aplicación asignada, se instala a petición.

El instalador admite el anuncio de aplicaciones y características según el sistema operativo. El instalador registra la información de clase COM para las aplicaciones asignadas a partir Windows XP. Esto permite al instalador instalar la aplicación tras la creación de una instancia de una clase anunciada. Para obtener más información, vea [Compatibilidad con plataformas de anuncios.](platform-support-of-advertisement.md)

Puede publicar una aplicación desde el servidor a partir de Windows Server 2003. A continuación, la aplicación publicada se instala a través de su asociación de archivos o el tipo de extensión de correo de Internet multipropósito (MIME). La publicación no rellena la interfaz de usuario con ninguno de los iconos de la aplicación. El sistema operativo cliente puede instalar una aplicación publicada a partir de Windows XP.

 

 



