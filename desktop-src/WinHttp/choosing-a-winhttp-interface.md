---
description: Antes de empezar a desarrollar una aplicación de Servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si desea usar la API de C/C++ o la interfaz COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Elección de una interfaz WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7772959bd76dc7a257abc180c915f99df988a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474540"
---
# <a name="choosing-a-winhttp-interface"></a>Elección de una interfaz WinHTTP

Antes de empezar a desarrollar una aplicación de Servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si desea usar la API de C/C++ o la interfaz COM. En la tabla siguiente se resumen las ventajas y desventajas asociadas a cada uno de estos enfoques.




|  | C/C++ API | Interfaz COM | 
|--|-----------|---------------|
| Ventajas | <ul><li>Las respuestas se pueden procesar en fragmentos, lo que es más eficaz.</li><li>Las operaciones POST también se pueden procesar en fragmentos, lo que acelera el tiempo de procesamiento.</li><li>Compatibilidad con AutoProxy.</li><li>Acceso al conjunto completo de características de WinHTTP.</li><li>Los datos binarios se pueden controlar fácilmente.</li></ul> | <ul><li>La creación de una aplicación es fácil y requiere menos líneas de código que la API de C/C++.</li><li>Los lenguajes de scripting pueden usar la interfaz .</li></ul> | 
| Inconvenientes | <ul><li>El procesamiento es más complejo.</li><li>La API de C/C++ requiere más pasos que la interfaz COM para realizar las mismas acciones.</li><li>La configuración de una solicitud requiere más código.</li></ul> | <ul><li>La interfaz COM no proporciona acceso al conjunto completo de características de WinHTTP.</li><li>Es difícil controlar los tipos de datos binarios en algunos lenguajes de scripting, como VBScript y JScript.</li><li>La interfaz COM no admite AutoProxy.</li><li>Las aplicaciones deben usar el modelo de APARTMENT_THREADED COM.</li><li>Antes de que una respuesta pueda comenzar a procesarse, se debe recibir y almacenar en búfer toda la respuesta.</li></ul> | 




 

 

 



