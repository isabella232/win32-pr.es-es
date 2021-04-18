---
description: Antes de empezar a desarrollar una aplicación de servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si va a usar la API de C/C++ o la interfaz COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Elección de una interfaz WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716221"
---
# <a name="choosing-a-winhttp-interface"></a>Elección de una interfaz WinHTTP

Antes de empezar a desarrollar una aplicación de servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si va a usar la API de C/C++ o la interfaz COM. En la tabla siguiente se resumen las ventajas y desventajas asociadas a cada uno de estos enfoques.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>API DE C/C++</th>
<th>Interfaz COM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ventajas</td>
<td><ul>
<li>Las respuestas se pueden procesar en fragmentos, lo que es más eficaz.</li>
<li>Las operaciones POST también se pueden procesar en fragmentos y acelerar el tiempo de procesamiento.</li>
<li>Compatibilidad con AutoProxy.</li>
<li>Acceso al conjunto completo de características de WinHTTP.</li>
<li>Los datos binarios se pueden controlar fácilmente.</li>
</ul></td>
<td><ul>
<li>Crear una aplicación es fácil y requiere menos líneas de código que la API de C/C++.</li>
<li>La interfaz se puede usar en los lenguajes de scripting.</li>
</ul></td>
</tr>
<tr class="even">
<td>Inconvenientes</td>
<td><ul>
<li>El procesamiento es más complejo.</li>
<li>La API de C/C++ requiere más pasos que la interfaz COM para realizar las mismas acciones.</li>
<li>La configuración de una solicitud requiere más código.</li>
</ul></td>
<td><ul>
<li>La interfaz COM no proporciona acceso al conjunto completo de características de WinHTTP.</li>
<li>Es difícil administrar los tipos de datos binarios en algunos lenguajes de scripting, como VBScript y JScript.</li>
<li>La interfaz COM no es compatible con el proxy de.</li>
<li>Las aplicaciones deben utilizar el modelo de APARTMENT_THREADED COM.</li>
<li>Antes de que se pueda empezar a procesar una respuesta, primero se debe recibir y almacenar en búfer la respuesta completa.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



