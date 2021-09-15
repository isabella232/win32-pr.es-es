---
description: El archivo DLL del reconocedor debe estar registrado para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el Registro durante la instalación.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registro del archivo DLL de Recognizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574456"
---
# <a name="registering-your-recognizer-dll"></a>Registro del archivo DLL de Recognizer

El archivo DLL del reconocedor debe estar registrado para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el Registro durante la instalación.

Agregue una nueva clave para cada uno de los CLID del reconocedor en la clave del Registro HKEY \_ LOCAL \_ MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/. Agregue un CLSID por idioma. En la tabla siguiente se describen los valores que se deben agregar debajo de cada una de las claves que contienen los CLSID.

> [!Note]  
> Los nombres de estos valores distinguen mayúsculas de minúsculas.

 



| Nombre del valor                             | Tipo de valor             | Descripción del valor                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Marcas de funcionalidad del reconocedor<br/> | REG \_ DWORD<br/>  | DWORD usado para determinar las funcionalidades del reconocedor.<br/>                                                                                                                                                                                                                                                                                                                             |
| Recognizer DLL<br/>              | REG \_ SZ<br/>     | Ruta de acceso completa al archivo DLL del reconocedor instalado.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Idiomas reconocidos<br/>        | REG \_ BINARY<br/> | Matriz binaria que describe el idioma o los idiomas con los que un reconocedor está diseñado para trabajar.<br/> En rectypes.h, max languages define especifica el número máximo de idiomas admitidos por un reconocedor y cada idioma toma una palabra para almacenar en el elemento \_ "Idiomas reconocidos". El tamaño de la entrada del Registro REG \_ BINARY debe ser MAX \_ LANGUAGES \* sizeof(WORD).<br/> |



 

 

 




