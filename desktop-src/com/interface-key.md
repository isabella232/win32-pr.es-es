---
title: Clave de interfaz
description: Registra nuevas interfaces asociando un nombre de interfaz a un identificador de interfaz (IID). Debe haber una subclave IID para cada nueva interfaz.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Interfaz de la clave del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076081"
---
# <a name="interface-key"></a>Clave de interfaz

Registra nuevas interfaces asociando un nombre de interfaz a un identificador de interfaz (IID). Debe haber una subclave IID para cada nueva interfaz.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_Interfaz de \\ \\ clases de \\ software de máquina local** \\ *{* IID *}*



| Valor del Registro                               | Descripción                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifica la interfaz de la que se deriva la interfaz actual.                                  |
| [**NumMethods**](nummethods.md)             | Contiene el número de métodos de la interfaz asociada, incluidos los métodos de las interfaces derivadas. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Asigna un IID a un CLSID en archivos dll de proxy de 16 bits.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Asigna un IID a un CLSID en dll de proxy de 32 bits.                                                           |



 

## <a name="remarks"></a>Observaciones

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz**](interface.md)
</dt> </dl>

 

 




