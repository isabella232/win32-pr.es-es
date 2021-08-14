---
title: DataFormats
description: Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Com de clave del Registro DataFormats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310603"
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

## <a name="remarks"></a>Comentarios

El *valor file/format* especifica el formato de objeto o archivo principal predeterminado para los objetos de esta clase.

El *valor* formats especifica una lista de formatos para las implementaciones predeterminadas de [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), donde *n* es un índice entero de base cero. Por ejemplo, *n* formato , aspecto , medio , marca , donde formato es un formato del Portapapeles, aspecto es uno o varios miembros de  =     [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medio*   es uno o más miembros de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)y *marca* es uno o varios miembros de [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




