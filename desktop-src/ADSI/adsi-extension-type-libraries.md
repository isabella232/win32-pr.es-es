---
title: Bibliotecas de tipos de extensión ADSI
description: Las bibliotecas de tipos de las extensiones no se combinan.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI Extension Type Libraries ADSI
- extensiones ADSI, bibliotecas de tipos de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180835"
---
# <a name="adsi-extension-type-libraries"></a>Bibliotecas de tipos de extensión ADSI

Las bibliotecas de tipos de las extensiones no se combinan. Los clientes ADSI deben incluir específicamente la biblioteca de tipos para cada extensión. La biblioteca de tipos es necesaria para Visual Basic habilitar los enlaces anticipados. Las aplicaciones cliente escritas en C/C++ pueden llamar al **método QueryInterface** en las interfaces de extensión definidas en los archivos de encabezado de extensión.

 

 




