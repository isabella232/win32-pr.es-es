---
title: Propiedad VisibilityCause
description: Propiedad VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418738"
---
# <a name="visibilitycause-property"></a>Propiedad VisibilityCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor entero que especifica la causa del estado visible del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente*. **Caracteres ("***CharacterID***"). VisibilityCause**



| Value | Descripción                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | No se ha mostrado el carácter.                                                                            |
| 1     | El usuario ocultó el carácter con el comando en el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz. |
| 2     | El usuario mostró el carácter.                                                                               |
| 3     | La aplicación ocultó el carácter.                                                                          |
| 4     | La aplicación mostró el carácter.                                                                       |
| 5     | Otra aplicación cliente ocultó el carácter.                                                                |
| 6     | Otra aplicación cliente mostró el carácter.                                                             |
| 7     | El usuario ocultó el carácter con el comando en el menú emergente del carácter.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar esta propiedad para determinar qué causó el movimiento del carácter cuando más de una aplicación comparte (ha cargado) el mismo carácter. Estos valores son los mismos que los devueltos por los eventos [**Mostrar**](show-event.md) y [**ocultar**](hide-event.md) .

## <a name="see-also"></a>Consulte también

[**Ocultar evento**](hide-event.md), [**Mostrar evento**](show-event.md), [**ocultar método**](hide-method.md), [**Mostrar método**](show-method.md)


 

 




