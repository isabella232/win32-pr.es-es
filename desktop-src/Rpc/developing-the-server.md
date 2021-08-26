---
title: Desarrollo del servidor
description: Al crear un programa de servidor para una aplicación distribuida, debe usar el archivo de encabezado y el código auxiliar del servidor que genera el compilador MIDL.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- Llamada a procedimiento remoto RPC, tareas, desarrollo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efeba77168abe53e1df823f416c80a015cc63bc7b89c79a0a86d79174a7c78fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073414"
---
# <a name="developing-the-server"></a>Desarrollo del servidor

Al crear un programa de servidor para una aplicación distribuida, debe usar el archivo de encabezado y el código auxiliar del servidor que genera el compilador MIDL. Para obtener más información, [vea Desarrollar la interfaz](developing-the-interface.md). Incluya el archivo de encabezado en el archivo de programa C del servidor. Compile el código auxiliar del servidor con los archivos de código fuente de C que componen la aplicación. Vincule los archivos de objeto resultantes con la biblioteca de importación. Este proceso se ilustra en el diagrama siguiente.

![proceso de creación de un programa de servidor para una aplicación distribuida](images/srvrdev.png)

Como puede ver en el ejemplo de la ilustración, se usó un archivo MIDL denominado MyApp.idl para definir la interfaz. El compilador MIDL usó MyApp.idl para generar MyApp \_ s.c y MyApp.h. También genera un archivo de código fuente de C para el código auxiliar del cliente, pero eso no es pertinente para esta explicación concreta. El archivo de código fuente de C para el programa de servidor (en este caso, Mysrvr.c) debe incluir el archivo Myapp.h. También tendrá que incluir los archivos Rpc.h y Rpc rpc.h.

La aplicación de servidor se desarrolló en dos archivos, Mysrvr.c y Rprocs.c. El archivo Mysrvr.c contiene las funciones necesarias para poner en funcionamiento el programa del servidor. Los procedimientos remotos que ofrece el programa de servidor se encuentran en el archivo Rprocs.c.

Los archivos Mysrvr.c y Rprocs.c se compilaron junto con Myapp \_ s.c para generar archivos de objeto. A continuación, los archivos de objeto se vinculaban con la biblioteca en tiempo de ejecución rpc y con cualquier otra biblioteca que pudieran necesitar. El resultado es un programa de servidor ejecutable denominado Mysrvr.exe.

Si no compila el archivo IDL en el modo de compatibilidad de Open Software Foundation (OSF) ([**/osf**](/windows/desktop/Midl/-osf)), el programa de servidor debe proporcionar una función para asignar memoria y una función para desasignarla. Para Windows 2000 y versiones posteriores de Windows, el modo recomendado [**es /Oicf.**](/windows/desktop/Midl/-oi) Para obtener más información, vea [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), y [Pointers and Memory Allocation](pointers-and-memory-allocation.md).

 

 