---
title: El archivo de registro de interfaz
description: El archivo de registro de interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- MIDL del archivo de registro de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159351"
---
# <a name="the-interface-registration-file"></a>El archivo de registro de interfaz

El archivo de registro de interfaz recopila información que ayuda en el registro de interfaces COM empaquetadas en un archivo DLL o EXE. El archivo de registro de interfaz es diferente de otros archivos generados porque puede recopilar información de la compilación de varios archivos IDL diferentes. Cada ejecución del compilador MIDL para interfaces COM busca primero un archivo dlldata.c existente y, si no se encuentra, se crea un nuevo archivo dlldata.c. Si se encuentra un archivo dlldata.c, se agrega información sobre el IDL actual (si no existe) o se reemplaza.

El archivo de registro de interfaz se genera o actualiza de forma segura en un entorno de varios procesadores porque se impide que las compilaciones MIDL paralelas escriban en el archivo al mismo tiempo. Dado que el entorno de compilación o el usuario pueden marcar cualquier archivo dlldata.c como de solo lectura, el compilador midL implementa un enfoque de tiempo de espera para esperar en un archivo que no se puede abrir y emite un mensaje de error adecuado si expira el tiempo de espera.

El nombre predeterminado del archivo de registro de interfaz generado a partir de un archivo de entrada es dlldata.c. El modificador del compilador MIDL [**/dlldata**](-dlldata.md) se puede usar para invalidar el nombre predeterminado del archivo. Invalidar el nombre predeterminado del archivo de registro de interfaz es especialmente útil cuando algunos archivos IDL empaquetados en un binario común residen en directorios diferentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar y registrar un archivo DLL de proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 