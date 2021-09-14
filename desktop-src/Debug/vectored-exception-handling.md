---
description: Los controladores de excepciones vectoriales son una extensión para el control estructurado de excepciones.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Control de excepciones vectoriales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164545"
---
# <a name="vectored-exception-handling"></a>Control de excepciones vectoriales

Los controladores de excepciones vectoriales son una extensión para el control estructurado de excepciones. Una aplicación puede registrar una función para ver o controlar todas las excepciones de la aplicación. Los controladores vectorados no están basados en fotogramas, por lo que puede agregar un controlador al que se llamará independientemente de dónde se encuentra en un marco de llamada. Se llama a los controladores vectorados en el orden en que se agregaron, después de que el depurador reciba una notificación de primera oportunidad, pero antes de que el sistema comience a desenredlar la pila.

Para agregar un controlador continue vectored, use la [**función AddVectoredContinueHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) Para quitar este controlador, use la [**función RemoveVectoredContinueHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

Para agregar un controlador de excepciones vectoriales, use [**la función AddVectoredExceptionHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) Para quitar este controlador, use la [**función RemoveVectoredExceptionHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

 

 
