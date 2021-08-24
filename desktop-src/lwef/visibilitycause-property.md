---
title: Propiedad VisibilityCause
description: Propiedad VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398795"
---
# <a name="visibilitycause-property"></a>Propiedad VisibilityCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor entero que especifica lo que provocó el estado visible del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agente*. **Characters("**_CharacterID_*_"). VisibilityCause_*



| Value | Descripción                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | No se ha mostrado el carácter.                                                                            |
| 1     | El usuario ocultó el carácter mediante el comando en el menú emergente del icono de la barra de tareas del carácter o mediante la entrada de voz. |
| 2     | El usuario mostró el carácter.                                                                               |
| 3     | La aplicación ocultó el carácter.                                                                          |
| 4     | La aplicación mostró el carácter.                                                                       |
| 5     | Otra aplicación cliente ocultó el carácter.                                                                |
| 6     | Otra aplicación cliente mostró el carácter.                                                             |
| 7     | El usuario ocultó el carácter mediante el comando en el menú emergente del carácter.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar esta propiedad para determinar qué ha provocado que el carácter se mueva cuando más de una aplicación comparte (ha cargado) el mismo carácter. Estos valores son los mismos que los devueltos por los [**eventos Show**](show-event.md) [**y Hide.**](hide-event.md)

## <a name="see-also"></a>Consulte también

[**Hide event**](hide-event.md), [**Show event**](show-event.md), Hide [**method**](hide-method.md), [**Show method**](show-method.md)


 

 




