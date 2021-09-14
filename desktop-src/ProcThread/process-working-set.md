---
description: El conjunto de trabajo de un programa es una colección de esas páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Conjunto de trabajo de proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062810"
---
# <a name="process-working-set"></a>Conjunto de trabajo de proceso

El *conjunto de trabajo* de un programa es una colección de esas páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente. Incluye datos compartidos y privados. Los datos compartidos incluyen páginas que contienen todas las instrucciones que ejecuta la aplicación, incluidas las de los archivos DLL y los archivos DLL del sistema. A medida que aumenta el tamaño del espacio de trabajo, aumenta la demanda de memoria.

Un proceso tiene asociado un tamaño mínimo de espacio de trabajo y un tamaño máximo del espacio de trabajo. Cada vez que se [**llama a CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)se reserva el tamaño mínimo del espacio de trabajo para el proceso. El administrador de memoria virtual intenta mantener suficiente memoria para el espacio de trabajo mínimo que residen cuando el proceso está activo, pero no mantiene un tamaño superior al máximo.

Para obtener los tamaños mínimo y máximo solicitados del espacio de trabajo para la aplicación, llame a la [**función GetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)

El sistema establece los tamaños predeterminados del conjunto de trabajo. También puede modificar los tamaños del conjunto de trabajo mediante la [**función SetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) Establecer estos valores no es una garantía de que la memoria se reservará o será residentes. Tenga cuidado al solicitar un tamaño de espacio de trabajo mínimo o máximo demasiado grande, ya que hacerlo puede degradar el rendimiento del sistema.

Para obtener el tamaño actual o máximo del conjunto de trabajo para el proceso, use la [**función GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de rendimiento de memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Espacio de trabajo](../memory/working-set.md)
</dt> </dl>

 

 
