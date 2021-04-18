---
description: Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modos de reinstalación de los ensamblados de Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667149"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Modos de reinstalación de los ensamblados de Common Language Runtime

Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado. Esto significa que los modos de reinstalación usados por [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) y [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) deben tener significados diferentes para los componentes normales y los ensamblados de Common Language Runtime. Las siguientes definiciones de modos de reinstalación se aplican a ensamblados de Common Language Runtime.



| Modo de reinstalación                  | Significado de los componentes de Microsoft .NET                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| REINSTALLMODE \_ FILEMISSING      | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEOLDERVERSION | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEEQUALVERSION | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEEXACT        | Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.                                         |
| REINSTALLMODE \_ FILEVERIFY       | Instale o vuelva a instalar el componente de Common Language Runtime si falta o si el componente existente está incompleto o dañado. |
| REINSTALLMODE \_ FILEREPLACE      | Instale o vuelva a instalar siempre el componente Common Language Runtime.                                                                 |



 

 

 



