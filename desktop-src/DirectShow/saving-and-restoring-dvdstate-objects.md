---
description: Guardar y restaurar objetos DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Guardar y restaurar objetos DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922851cce72f736364c1f1e66b24032586221ad9cb75494c7286fe962eb34403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982575"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Guardar y restaurar objetos DvdState

Los objetos [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permiten a las aplicaciones guardar una instantánea de la sesión de usuario, incluida información como la ubicación actual en el disco, el nivel parental de la persona que está viendo, los flujos de audio y subapictura seleccionados, y así sucesivamente. Esto significa que los usuarios pueden guardar su lugar en un disco DVD-Video disco y verlo más adelante.

Las aplicaciones no pueden crear objetos DvdState. El navegador de DVD crea internamente estos objetos cuando una aplicación llama a [**IDvdInfo2::GetState.**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate) Los objetos DvdState exponen la [**interfaz IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) para permitir que las aplicaciones consulten cierta información.

En la aplicación de ejemplo de DVD, las funciones **CDvdCore::RestoreBookmark** y **CDvdCore::SaveBookmark** muestran cómo guardar y recuperar objetos DvdState.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



