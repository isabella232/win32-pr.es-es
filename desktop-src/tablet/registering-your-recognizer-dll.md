---
description: La DLL del reconocedor debe estar registrada para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el registro durante la instalación.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registro de la DLL del reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547059"
---
# <a name="registering-your-recognizer-dll"></a>Registro de la DLL del reconocedor

La DLL del reconocedor debe estar registrada para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el registro durante la instalación.

Agregue una nueva clave para cada uno de los CLSID del reconocedor en la \_ \_ clave del registro HKEY local Machine/software/Microsoft/TPG/reconocedores/. Agregue un CLSID por idioma. En la tabla siguiente se describen los valores que se deben agregar debajo de cada una de las claves que contienen los CLSID.

> [!Note]  
> Los nombres de estos valores distinguen mayúsculas de minúsculas.

 



| Nombre del valor                             | Tipo de valor             | Descripción del valor                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Marcas de capacidad del reconocedor<br/> | \_valor DWORD reg<br/>  | DWORD que se usa para determinar las capacidades del reconocedor.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL del reconocedor<br/>              | Registro \_ SZ<br/>     | Ruta de acceso completa al archivo DLL del reconocedor instalado.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Idiomas reconocidos<br/>        | \_binario de reg<br/> | Matriz binaria que describe el idioma o los idiomas con los que está diseñado un reconocedor.<br/> En rectypes. h, la \_ definición de idiomas Max especifica el número máximo de idiomas admitidos por un reconocedor y cada idioma toma una palabra para almacenar en el elemento "idiomas reconocidos". El tamaño de la \_ entrada del registro reg Binary debe ser Max \_ Language \* sizeof (Word).<br/> |



 

 

 




