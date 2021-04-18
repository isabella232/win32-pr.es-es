---
title: El archivo de registro de la interfaz
description: El archivo de registro de la interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- archivo de registro de interfaz MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665813"
---
# <a name="the-interface-registration-file"></a>El archivo de registro de la interfaz

El archivo de registro de la interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE. El archivo de registro de la interfaz es diferente de otros archivos generados porque puede recopilar información de la compilación de varios archivos IDL diferentes. Cada ejecución del compilador de MIDL para interfaces COM busca primero un archivo dlldata. c existente y, si no se encuentra el archivo, se crea un nuevo archivo dlldata. c. Si se encuentra un archivo dlldata. c, se agrega información sobre el IDL actual (si no existe) o se reemplaza.

El archivo de registro de la interfaz se genera o actualiza de forma segura en un entorno con varios procesadores porque las compilaciones MIDL paralelas no pueden escribir en el archivo al mismo tiempo. Dado que cualquier archivo dlldata. c puede marcarse como de solo lectura en el entorno de compilación o el usuario, el compilador MIDL implementa un enfoque de tiempo de espera para esperar en un archivo que no se puede abrir y emite un mensaje de error adecuado si el tiempo de espera expira.

El nombre predeterminado del archivo de registro de la interfaz generado a partir de un archivo de entrada es dlldata. c. El modificador de compilador MIDL [**/dlldata**](-dlldata.md) se puede usar para reemplazar el nombre predeterminado del archivo. Reemplazar el nombre predeterminado del archivo de registro de la interfaz es especialmente útil cuando algunos archivos IDL empaquetados en un binario común residen en directorios diferentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar y registrar un archivo DLL de proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 