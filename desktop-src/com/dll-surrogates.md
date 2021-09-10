---
title: Suplentes de DLL
description: Suplentes de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369715"
---
# <a name="dll-surrogates"></a>Suplentes de DLL

COM permite crear servidores DLL que se pueden cargar en un proceso EXE suplente. Esto combina la facilidad de escribir servidores DLL con las ventajas de la implementación ejecutable. Las herramientas de desarrollo Microsoft Visual Studio facilitan la escritura de servidores DLL, pero un servidor DLL en sí mismo tiene límites. Ejecutar el servidor DLL en un proceso suplente ofrece varias ventajas posibles:

-   Aislamiento de errores y la capacidad de dar servicio a varios clientes simultáneamente.
-   En un entorno distribuido, se podría usar una implementación de servidor DLL para dar servicio a clientes remotos.
-   Podría permitir que los clientes ayudaran a protegerse del código de servidor que no es de confianza, a la vez que les permitía acceder a los servicios que proporciona el servidor DLL.
-   La ejecución de un servidor DLL en un suplente proporciona al archivo DLL la seguridad del suplente.

COM proporciona un proceso suplente predeterminado o puede escribir un suplente personalizado si tiene necesidades especiales.

En los temas siguientes se proporciona más información sobre los suplentes de DLL:

-   [Requisitos del servidor DLL](dll-server-requirements.md)
-   [Uso de System-Supplied suplente](using-the-system-supplied-surrogate.md)
-   [Escritura de un suplente personalizado](writing-a-custom-surrogate.md)

 

 




