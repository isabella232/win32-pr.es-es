---
description: Funciones avx de Intel.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Funciones de AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d4645fc9869931e094fa6fd84a8c5b79b1ff09a6fcfd65df3f3b043fe84573
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815615"
---
# <a name="avx-functions"></a>Funciones de AVX

Las siguientes son las funciones avx de Intel.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                   | Descripción                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**CopyContext**](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | Copia una estructura de contexto de origen (incluido cualquier XState) en una estructura de contexto de destino inicializada.<br/>         |
| [**GetEnabledXStateFeatures**](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | Obtiene una máscara de características XState habilitadas en procesadores x86 o x64.<br/>                                                    |
| [**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | Devuelve la máscara de las características XState establecidas dentro de una [**estructura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)<br/>                        |
| [**InitializeContext**](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | Inicializa una estructura [**CONTEXT dentro**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) de un búfer con el tamaño y la alineación necesarios.<br/>       |
| [**LocateXStateFeature**](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | Recupera un puntero al estado del procesador para una característica XState dentro de una [**estructura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)<br/> |
| [**SetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | Establece la máscara de las características de XState establecidas dentro de una [**estructura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)<br/>                             |



 

 

 




