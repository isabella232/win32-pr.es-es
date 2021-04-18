---
title: Suplentes DLL
description: Suplentes DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714258"
---
# <a name="dll-surrogates"></a>Suplentes DLL

COM permite crear servidores DLL que se pueden cargar en un proceso EXE suplente. Esto combina la facilidad de escritura de servidores DLL con las ventajas de la implementación ejecutable. Las herramientas de desarrollo como Microsoft Visual Studio facilitan la escritura de servidores DLL, pero un servidor DLL en sí mismo tiene límites. La ejecución del servidor DLL en un proceso suplente ofrece varias ventajas posibles:

-   Aislamiento de errores y la capacidad de atender a varios clientes simultáneamente.
-   En un entorno distribuido, se puede usar una implementación de servidor DLL para atender a los clientes remotos.
-   Puede permitir que los clientes ayuden a protegerse del código de servidor que no es de confianza, a la vez que permiten el acceso a los servicios que proporciona el servidor DLL.
-   La ejecución de un servidor DLL en un suplente proporciona el archivo DLL con la seguridad del suplente.

COM proporciona un proceso suplente predeterminado, o puede escribir un suplente personalizado si tiene necesidades especiales.

En los temas siguientes se proporciona más información sobre los suplentes de DLL:

-   [Requisitos del servidor DLL](dll-server-requirements.md)
-   [Usar el suplente System-Supplied](using-the-system-supplied-surrogate.md)
-   [Escritura de un suplente personalizado](writing-a-custom-surrogate.md)

 

 




