---
description: Los terminales conectables se clasifican en superclases de terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entradas del registro (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689552"
---
# <a name="registry-entries-telephony-api"></a>Entradas del registro (API de telefonía)

Los terminales conectables se clasifican en superclases de terminal. Cada superclase de terminal tiene una entrada en el registro con la siguiente clave:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telephony** \\ **TerminalManager**

Debajo de la clave de la superclase de terminal hay entradas para cada terminal acoplable en la superclase de terminal.

La entrada de cada superclase de terminal se identifica mediante un CLSID de la superclase de terminal. Se trata de un identificador único para una clase de terminal. La clase terminal tiene un atributo opcional: Name, que es un nombre descriptivo para la clase terminal. Cada terminal acoplable se identifica mediante una clase terminal CLSID; es decir, un GUID. Los atributos del terminal acoplable se almacenan en valores de clave de terminal conectables. Los atributos de un terminal acoplable son los siguientes.



| Clase terminal | Nombre de clave | Identificador público                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nombre           | Registro \_ SZ  | Nombre descriptivo del terminal                                                            |
| Compañía        | Registro \_ SZ  | Nombre de la compañía                                                                      |
| Versión        | Registro \_ SZ  | Información de la versión                                                               |
| CLSID          | Registro \_ SZ  | Terminal CLSID (se usa en el método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) de com) |
| Direcciones     | DWORD    | Dirección del terminal                                                                |
| MediaTypes     | DWORD    | Tipos de medios de terminal compatibles                                                    |



 

En el caso de una clase terminal, los atributos son los siguientes.



| CLSID | Nombre de clave | Identificador público            |
|-------|----------|------------------------------|
| Nombre  | Registro \_ SZ  | Nombre descriptivo de la clase de terminal |



 

 

 
