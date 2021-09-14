---
title: Errores comunes (AD DS)
description: La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Errores comunes de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02b1006cab476ca042a0026e66132af44cbaed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070208"
---
# <a name="common-errors-ad-ds"></a>Errores comunes (AD DS)

La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.




| HRESULT | Descripción | 
|---------|-------------|
| 0x8007001F | Error general. Este error se produce si intenta:<ul><li>Agregue un grupo local de dominio a un grupo global o universal o a un grupo local de dominio en otro dominio. Los grupos locales de dominio solo se pueden agregar como miembros a otros grupos locales de dominio del mismo dominio.</li><li>Agregue un grupo universal a un grupo global. Los grupos universales se pueden agregar a grupos locales universales y de dominio, pero no a grupos globales.</li></ul> | 
| 0x8007202F | <strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Este error se produce si intenta agregar un grupo de seguridad a otro grupo de un dominio que se ejecuta en modo mixto. Los grupos de seguridad no se pueden anidar en modo mixto; los grupos de seguridad solo se pueden anidar en modo nativo. | 




 

 

 




