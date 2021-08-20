---
description: Los terminales conectables se clasifican en superclases de terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entradas del Registro (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd6e4e4d91b65e3ef886fd4d2d44b571f4ac4696697aef8b8d8b2715e273e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761172"
---
# <a name="registry-entries-telephony-api"></a>Entradas del Registro (API de telefonía)

Los terminales conectables se clasifican en superclases de terminal. Cada superclase de Terminal tiene una entrada en el Registro bajo la siguiente clave:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **TerminalManager** de \\ **telefonía CurrentVersion** \\ 

Debajo de la clave De terminal superclase hay entradas para cada terminal conectable dentro de la superclase terminal.

La entrada de cada superclase de terminal se identifica mediante un CLSID de superclase de terminal. Se trata de un identificador único para una clase de terminal. La clase de terminal tiene un atributo opcional: name, que es un nombre descriptivo para la clase de terminal. Cada terminal conectable se identifica mediante una clase de terminal CLSID; es decir, un GUID. Los atributos del terminal conectable se almacenan en valores de clave de terminal conectables. Los atributos de un terminal conectable son los siguientes.



| Clase de terminal | Nombre de clave | Identificador público                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nombre           | REG \_ SZ  | Nombre descriptivo del terminal                                                            |
| Compañía        | REG \_ SZ  | Nombre de la compañía                                                                      |
| Versión        | REG \_ SZ  | Información de la versión                                                               |
| CLSID          | REG \_ SZ  | CLSID de terminal (se usa en el [**método COM CoCreateInstance)**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) |
| Direcciones     | DWORD    | Dirección del terminal                                                                |
| MediaTypes     | DWORD    | Tipos de medios de terminal admitidos                                                    |



 

Para una clase de terminal, los atributos son los siguientes.



| CLSID | Nombre de clave | Identificador público            |
|-------|----------|------------------------------|
| Nombre  | REG \_ SZ  | Nombre descriptivo de la clase terminal |



 

 

 
