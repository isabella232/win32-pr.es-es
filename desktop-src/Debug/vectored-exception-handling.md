---
description: Los controladores de excepciones de vectores son una extensión del control estructurado de excepciones.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Control de excepciones vectoriales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907229"
---
# <a name="vectored-exception-handling"></a>Control de excepciones vectoriales

Los controladores de excepciones de vectores son una extensión del control estructurado de excepciones. Una aplicación puede registrar una función para ver o controlar todas las excepciones de la aplicación. Los controladores vectoriales no están basados en marcos; por lo tanto, puede Agregar un controlador que se llamará independientemente de dónde se encuentre en un marco de llamada. Se llama a los controladores vectoriales en el orden en que se agregaron, después de que el depurador obtenga una notificación de primera oportunidad, pero antes de que el sistema comience a desenredar la pila.

Para agregar un controlador de continuación de vectores, utilice la función [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) . Para quitar este controlador, utilice la función [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .

Para agregar un controlador de excepciones vectoriales, utilice la función [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) . Para quitar este controlador, utilice la función [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .

 

 
