---
title: Clave de interfaz
description: Registra nuevas interfaces asociando un nombre de interfaz con un identificador de interfaz (IID). Debe haber una subclave IID para cada nueva interfaz.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- COM de clave del Registro de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda0cc29331521025a9274dca7b85080be2ddd5a9b631d2660eadaa13fe4941a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048153"
---
# <a name="interface-key"></a>Clave de interfaz

Registra nuevas interfaces asociando un nombre de interfaz con un identificador de interfaz (IID). Debe haber una subclave IID para cada nueva interfaz.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Interfaz \_ de clases DE SOFTWARE DE MÁQUINA \\ \\ \\ LOCAL** \\ *{* IID *}*



| Valor del Registro                               | Descripción                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifica la interfaz de la que se deriva la interfaz actual.                                  |
| [**NumMethods**](nummethods.md)             | Contiene el número de métodos de la interfaz asociada, incluidos los métodos de las interfaces derivadas. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Mapas un IID a un CLSID en archivos DLL de proxy de 16 bits.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Mapas un IID a un CLSID en archivos DLL de proxy de 32 bits.                                                           |



 

## <a name="remarks"></a>Comentarios

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz**](interface.md)
</dt> </dl>

 

 




