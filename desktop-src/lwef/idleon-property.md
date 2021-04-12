---
title: Idleon (propiedad)
description: Idleon (propiedad)
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356652"
---
# <a name="idleon-property"></a>Idleon (propiedad)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece un valor booleano que determina si el servidor administra las animaciones de estado de **ralentí** del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Idleon* *  \[  =  *Boolean*\]

</dd> </dl> 

| Parte      | Descripción                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el servidor administra el modo de inactividad. **True** (valor predeterminado) el control de servidor del estado de inactividad está habilitado. <br/> **False** El control de servidor del estado de inactividad está deshabilitado. <br/> |



 

## <a name="remarks"></a>Observaciones

El servidor establece automáticamente un tiempo de espera después de la última animación reproducida para un carácter. Una vez completado el intervalo de este temporizador, el servidor inicia el estado de **ralentí** para un carácter y reproduce sus animaciones de inactiva **asociadas a intervalos** regulares. Si desea deshabilitar el servidor para que reproduzca automáticamente las animaciones de estado de **ralentí** , establezca la propiedad en **false** y reproduzca una animación o llame al método [**Stop**](stop-method.md) . El establecimiento de este valor no afecta al estado de animación actual del carácter.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 





