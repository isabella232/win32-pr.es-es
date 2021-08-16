---
description: Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie. Por ejemplo, una superficie que representa un mapa de un juego puede contener información sobre el terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Datos de superficie privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c010e24f691dc64c75e4dcea428af21d46ebfcb95b31775b9c8db81b2263e6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520197"
---
# <a name="private-surface-data-direct3d-9"></a>Datos de superficie privada (Direct3D 9)

Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie. Por ejemplo, una superficie que representa un mapa de un juego puede contener información sobre el terreno.

Una superficie puede tener más de un búfer de datos privado. Cada búfer se identifica mediante un GUID que se proporciona al adjuntar los datos a la superficie.

Para almacenar datos de superficie privada, use SetPrivateData, pasando un puntero al búfer de origen, el tamaño de los datos y un GUID definido por la aplicación para los datos. Opcionalmente, los datos de origen pueden existir en forma de objeto COM; En este caso, se pasa un puntero al puntero de interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto y se establece la marca D3DSPD \_ IUNKNOWNPOINTER.

SetPrivateData asigna un búfer interno para los datos y lo copia. A continuación, puede liberar de forma segura el búfer u objeto de origen. Cuando se llama a FreePrivateData, se libera la referencia de búfer o interfaz interna. Esto sucede automáticamente cuando se libera la superficie.

Para recuperar datos privados para una superficie, debe asignar un búfer del tamaño correcto y, a continuación, llamar al método GetPrivateData, pasando el GUID que se asignó a los datos. Usted es responsable de liberar cualquier memoria dinámica que use para este búfer. Si los datos son un objeto COM, este método recupera el [**puntero IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Si no sabe cuál es el tamaño de un búfer para asignar, primero llame a GetPrivateData con cero en pSizeOfData. Si se produce un error en el método con D3DERR \_ MOREDATA, devuelve el número necesario de bytes para el búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
