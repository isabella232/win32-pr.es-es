---
description: Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modos de reinstalación de ensamblados de Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074324"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Modos de reinstalación de ensamblados de Common Language Runtime

Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado. Esto significa que los modos de reinstalación usados por [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) y [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) deben tener significados diferentes para los componentes normales y los ensamblados de Common Language Runtime. Las siguientes definiciones de modos de reinstalación se aplican a los ensamblados de Common Language Runtime.



| Modo de reinstalación                  | Significado para Microsoft .NET componentes                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| REINSTALLMODE \_ FILEMISSING      | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEOLDERVERSION | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEEQUALVERSION | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEEXACT        | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEVERIFY       | Instale o vuelva a instalar el componente de Common Language Runtime si falta o si el componente existente está incompleto o dañado. |
| REINSTALLMODE \_ FILEREPLACE      | Instale o vuelva a instalar siempre el componente de Common Language Runtime.                                                                 |



 

 

 



