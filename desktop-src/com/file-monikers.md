---
title: File Monikers
description: File Monikers
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369508"
---
# <a name="file-monikers"></a>File Monikers

*Los monikers de archivo* son la clase de moniker más sencilla. Los monikers de archivo se pueden usar para identificar cualquier objeto almacenado en su propio archivo. Un moniker de archivo actúa como contenedor para el nombre de ruta de acceso que el sistema de archivos nativo asigna al archivo. Llamar [**a IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) para este moniker provocaría que este objeto se activara y, a continuación, devolvería un puntero de interfaz al objeto . El origen del objeto denominado por el moniker debe proporcionar una implementación de la [**interfaz IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) para admitir el enlace de un moniker de archivo. Los monikers de archivo pueden representar una ruta de acceso completa o relativa.

Por ejemplo, el moniker de archivo para un objeto de hoja de cálculo almacenado como el archivo C: WorkMySheet.xls incluiría información equivalente a ese \\ nombre de ruta de \\ acceso. Sin embargo, el moniker no constaría necesariamente de la misma cadena. La cadena es simplemente su *nombre para* mostrar, una representación del contenido del moniker que es significativo para un usuario final. El nombre para mostrar, que está disponible a través del método [**IMoniker::GetDisplayName,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) solo se usa al mostrar un moniker a un usuario final. Este método obtiene el nombre para mostrar de cualquiera de las clases de moniker. Internamente, el moniker puede almacenar la misma información en un formato que sea más eficaz para realizar operaciones de moniker, pero que no sea significativo para los usuarios. A continuación, cuando este mismo objeto se enlaza a través de una llamada al método [**BindToObject,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) el objeto se activaría, probablemente cargando el archivo en la hoja de cálculo.

OLE ofrece a los proveedores de moniker la función auxiliar [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) que crea un objeto moniker de archivo y devuelve su puntero al proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de elementos](item-monikers.md)
</dt> <dt>

[Pointer Monikers](pointer-monikers.md)
</dt> </dl>

 

 




