---
title: El archivo UUID de interfaz
description: El archivo UUID de interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces del archivo IDL procesado.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL y COM MIDL, interfaces, archivos UUID de proxy
- MIDL del archivo UUID de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159350"
---
# <a name="the-interface-uuid-file"></a>El archivo UUID de interfaz

El archivo UUID de interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces del archivo IDL procesado. Al igual que el archivo de código auxiliar y el archivo de encabezado, el cierre del flujo de entrada se define mediante el archivo IDL actual y los archivos incluidos. Por ejemplo, para Interface IFace, el compilador genera un IFace de IID constante y lo inicializa en el UUID de la interfaz especificado en el \_ archivo IDL. Las aplicaciones cliente y el archivo DLL de proxy usan esta constante para identificar la interfaz.

El nombre predeterminado de un archivo IID de interfaz generado a partir de file.idl es File \_ i.c. El [**modificador del compilador /iid**](-iid.md) MIDL invalida el nombre predeterminado del archivo UUID de la interfaz.

 

 




