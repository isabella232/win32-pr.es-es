---
title: Los archivos de encabezado
description: El archivo de encabezado de interfaz (Name.h) contiene definiciones de tipo y declaraciones de función basadas en la definición de interfaz en el archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la directiva \include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- archivos de encabezado MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159357"
---
# <a name="the-header-files"></a>Los archivos de encabezado

El archivo de encabezado de interfaz (Name.h) contiene definiciones de tipo y declaraciones de función basadas en la definición de interfaz del archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la \# directiva include. Los tipos de datos de los archivos importados con la directiva import no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de include al archivo H generado a partir del archivo importado.

Incluya este archivo en los archivos de origen para el archivo DLL de proxy y para las aplicaciones cliente que usan la interfaz .

El nombre predeterminado de un archivo de encabezado generado a partir de file.idl es File.h. El [**modificador del compilador /header**](-header.md) MIDL invalida el nombre predeterminado del archivo de encabezado de interfaz.

 

 




