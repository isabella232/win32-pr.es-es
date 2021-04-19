---
title: Requisitos HTTP para descargas de BITS
description: BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486646"
---
# <a name="http-requirements-for-bits-downloads"></a>Requisitos HTTP para descargas de BITS

BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1. En el caso de las descargas, el método **principal** del servidor http debe devolver el tamaño del archivo y su método **Get** debe admitir los encabezados Content-Range y Content-Length. Como resultado, BITS solo transfiere el contenido del archivo estático y genera un error si se intenta transferir contenido dinámico, a menos que el script ASP, ISAPI o CGI admita los encabezados Content-Range y Content-Length.

BITS puede usar un servidor HTTP/1.0 siempre que cumpla los requisitos de los métodos **Head** y **Get** .

Para admitir la descarga de intervalos de un archivo, el servidor debe admitir los siguientes requisitos:

-   Permita que los encabezados MIME incluyan los encabezados Content-Range y Content-Type estándar, además de un máximo de 180 bytes de otros encabezados.
-   Permite un máximo de dos CR/LFs entre los encabezados HTTP y la primera cadena de límite.

 

 




