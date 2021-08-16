---
description: Obtiene el objeto ISearchItem si la dirección URL representa un origen de datos de Shell real (también conocido como extensión de espacio de nombres de Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: ISearchItem::GetParentFolder (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094916"
---
# <a name="isearchitemgetparentfolder-method"></a>ISearchItem::GetParentFolder (método)

Obtiene el [**objeto ISearchItem**](-search-isearchitem.md) si la dirección URL representa un origen de datos de Shell real (también conocido como extensión de espacio de nombres de Shell).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IShellFolder* \[ out\]
</dt> <dd>

Tipo: **ppShellFolder \* \***

Al devolver, contiene la dirección de un puntero a la carpeta que contiene la dirección URL actual. Todos los objetos de carpeta del espacio de nombres de Shell exponen la interfaz [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) y sus métodos se usan para administrar carpetas.

</dd> <dt>

*LPITEMIDLIST* \[ out\]
</dt> <dd>

Tipo: **\* pppdl**

Al devolver, contiene la dirección de un puntero a una lista de identificadores de elemento (PIDL) que identifica la carpeta primaria. El *parámetro LPITEMIDLIST* puede hacer referencia a un objeto en cualquier nivel por debajo de la carpeta primaria de la jerarquía de espacios de nombres y, por tanto, puede ser un puntero de varios niveles a un **pidl** relativo a la carpeta primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **método ISearchItem::GetParentFolder** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**ISearchItem**](-search-isearchitem.md) y las siguientes API: las interfaces [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI,**](-search-isearchprotocolui.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
