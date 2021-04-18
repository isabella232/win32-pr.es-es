---
description: Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie. Por ejemplo, una superficie que representa un mapa en un juego podría contener información sobre el terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Datos de la superficie privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714779"
---
# <a name="private-surface-data-direct3d-9"></a>Datos de la superficie privada (Direct3D 9)

Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie. Por ejemplo, una superficie que representa un mapa en un juego podría contener información sobre el terreno.

Una superficie puede tener más de un búfer de datos privado. Cada búfer se identifica mediante un GUID que se proporciona al adjuntar los datos a la superficie.

Para almacenar datos de la superficie privada, use SetPrivateData, pasando un puntero al búfer de origen, el tamaño de los datos y un GUID definido por la aplicación para los datos. Opcionalmente, los datos de origen pueden existir en el formulario de un objeto COM. en este caso, se pasa un puntero al puntero de interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto y se establece la \_ marca IUNKNOWNPOINTER de D3DSPD.

SetPrivateData asigna un búfer interno para los datos y lo copia. Después, puede liberar de forma segura el búfer de origen o el objeto. La referencia de búfer interno o de interfaz se libera cuando se llama a FreePrivateData. Esto sucede automáticamente cuando se libera la superficie.

Para recuperar los datos privados de una superficie, debe asignar un búfer con el tamaño correcto y, a continuación, llamar al método GetPrivateData y pasar el GUID que se asignó a los datos. Usted es responsable de liberar cualquier memoria dinámica que use para este búfer. Si los datos son un objeto COM, este método recupera el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Si no sabe lo grande que puede asignar un búfer, llame primero a GetPrivateData con cero en pSizeOfData. Si se produce un error en el método con D3DERR \_ MOREDATA, se devuelve el número de bytes necesario para el búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
