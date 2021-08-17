---
title: Requisitos HTTP para descargas de BITS
description: BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9bd997bb5ef7f2125cfe7c3dc6850c0f44e81a8c3138f7f130952e31202a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010880"
---
# <a name="http-requirements-for-bits-downloads"></a>Requisitos HTTP para descargas de BITS

BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1. Para las descargas, el método **Head** del servidor HTTP debe devolver el tamaño del archivo y su **método Get** debe admitir los encabezados Content-Range y Content-Length. Como resultado, BITS solo transfiere el contenido del archivo estático y genera un error si intenta transferir contenido dinámico, a menos que el script ASP, ISAPI o CGI admita los encabezados Content-Range y Content-Length.

BITS puede usar un servidor HTTP/1.0 siempre que cumpla los requisitos del método **Head** **y Get.**

Para admitir la descarga de intervalos de un archivo, el servidor debe admitir los siguientes requisitos:

-   Permita que los encabezados MIME incluyan los encabezados Content-Range y Content-Type estándar, además de un máximo de 180 bytes de otros encabezados.
-   Permita un máximo de dos CR/LF entre los encabezados HTTP y la primera cadena de límite.

 

 




