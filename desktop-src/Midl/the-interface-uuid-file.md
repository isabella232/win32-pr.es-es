---
title: El archivo UUID de la interfaz
description: El archivo UUID de la interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces en el archivo IDL procesado.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL y COM MIDL, interfaces, archivos UUID de proxy
- archivo UUID de interfaz MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778991"
---
# <a name="the-interface-uuid-file"></a>El archivo UUID de la interfaz

El archivo UUID de la interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces en el archivo IDL procesado. Al igual que el archivo de código auxiliar y el archivo de encabezado, el cierre del flujo de entrada se define mediante el archivo IDL actual y los archivos incluidos. Por ejemplo, para la interfaz IFace, el compilador genera un IID de constante \_ IFace y lo inicializa en el UUID de la interfaz especificado en el archivo IDL. Las aplicaciones cliente y el archivo DLL de proxy usan esta constante para identificar la interfaz.

El nombre predeterminado de un archivo IID de interfaz generado a partir de un archivo. idl es el archivo \_ i.c. El modificador de compilador de MIDL [**/IID**](-iid.md) invalida el nombre predeterminado del archivo UUID de interfaz.

 

 




