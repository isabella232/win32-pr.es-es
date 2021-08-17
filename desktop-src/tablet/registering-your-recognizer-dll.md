---
description: El archivo DLL del reconocedor debe estar registrado para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el Registro durante la instalación.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrar el archivo DLL de Recognizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae80eb49f1795e315cf77bf5aede83cc1677e168f4aea4d6715a216e74434caf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350075"
---
# <a name="registering-your-recognizer-dll"></a>Registrar el archivo DLL de Recognizer

El archivo DLL del reconocedor debe estar registrado para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el Registro durante la instalación.

Agregue una nueva clave para cada uno de los CLID del reconocedor en la clave del Registro HKEY \_ LOCAL \_ MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/. Agregue un CLSID por idioma. En la tabla siguiente se describen los valores que se deben agregar debajo de cada una de las claves que contienen los CLID.

> [!Note]  
> Los nombres de estos valores distinguen mayúsculas de minúsculas.

 



| Nombre del valor                             | Tipo de valor             | Descripción del valor                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Marcas de funcionalidad del reconocedor<br/> | REG \_ DWORD<br/>  | DWORD se usa para determinar las funciones del reconocedor.<br/>                                                                                                                                                                                                                                                                                                                             |
| Recognizer DLL<br/>              | REG \_ SZ<br/>     | Ruta de acceso completa al archivo DLL del reconocedor instalado.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Idiomas reconocidos<br/>        | REG \_ BINARY<br/> | Matriz binaria que describe el idioma o los idiomas con los que un reconocedor está diseñado para trabajar.<br/> En rectypes.h, la definición de MAX LANGUAGES especifica el número máximo de idiomas admitidos por un reconocedor y cada idioma toma una palabra para almacenar en el elemento \_ "Idiomas reconocidos". El tamaño de la entrada \_ del Registro REG BINARY debe ser MAX \_ LANGUAGES \* sizeof(WORD).<br/> |



 

 

 




