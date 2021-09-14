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
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360655"
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

En la devolución, contiene la dirección de un puntero a la carpeta que contiene la dirección URL actual. Todos los objetos de carpeta de espacio de nombres de Shell exponen la interfaz [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) y sus métodos se usan para administrar carpetas.

</dd> <dt>

*LPITEMIDLIST* \[ out\]
</dt> <dd>

Tipo: **\* pppdl**

En la devolución, contiene la dirección de un puntero a una lista de identificadores de elemento (PIDL) que identifica la carpeta primaria. El *parámetro LPITEMIDLIST* puede hacer referencia a un objeto en cualquier nivel debajo de la carpeta primaria de la jerarquía de espacios de nombres y, por tanto, puede ser un puntero de varios niveles a **un pidl** relativo a la carpeta primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El **método ISearchItem::GetParentFolder** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**ISearchItem**](-search-isearchitem.md) y las siguientes API: las interfaces [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI,**](-search-isearchprotocolui.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
