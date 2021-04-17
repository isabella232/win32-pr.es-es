---
title: DataFormats
description: Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Clave del registro de dataFormat COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704791"
---
# <a name="dataformats"></a>DataFormats

Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Observaciones

El valor de *archivo o formato* especifica el formato de archivo o objeto principal predeterminado para los objetos de esta clase.

El valor *Formats* especifica una lista de formatos para las implementaciones predeterminadas de [**del EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), donde *n* es un índice entero de base cero. Por ejemplo, *n*  =  *formato*, *aspecto*, *medio*, *marca*, donde *formato* es un formato de Portapapeles, el *aspecto* es uno o varios miembros de [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* es uno o más miembros de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)y *Flag* es uno o más miembros de [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDataObject:: del EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




