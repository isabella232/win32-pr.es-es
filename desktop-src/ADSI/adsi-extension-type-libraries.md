---
title: Bibliotecas de tipos de extensiones ADSI
description: Las bibliotecas de tipos para las extensiones no se combinan.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI Extensions de bibliotecas de tipos ADSI
- extensiones ADSI, bibliotecas de tipos de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531863"
---
# <a name="adsi-extension-type-libraries"></a>Bibliotecas de tipos de extensiones ADSI

Las bibliotecas de tipos para las extensiones no se combinan. Los clientes ADSI deben incluir específicamente la biblioteca de tipos para cada extensión. La biblioteca de tipos es necesaria para que Visual Basic habilite los enlaces iniciales. Las aplicaciones cliente escritas en C/C++ pueden llamar al método **QueryInterface** en las interfaces de extensión definidas en los archivos de encabezado de la extensión.

 

 




