---
description: Los métodos que se usan para trabajar con archivos de DirectX. x pueden devolver los siguientes valores además de los valores devueltos de COM estándar.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: Valores devueltos de D3DXFERR (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: cab1cc5e70b6204c832fd9fe5b0fecac4276f578
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157189"
---
# <a name="d3dxferr-return-values"></a>Valores devueltos de D3DXFERR

Los métodos que se usan para trabajar con archivos de DirectX. x pueden devolver los siguientes valores además de los valores devueltos de COM estándar.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ BADARRAYSIZE**
</dt> <dd>

Una matriz supera el tamaño permitido.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ BADCACHEFILE**
</dt> <dd>

No se pudo leer un archivo caché.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ BADDataReference**
</dt> <dd>

No se pudieron recuperar los datos de miembro de la plantilla.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ BADFILE**
</dt> <dd>

Error en una operación de lectura o escritura de archivo.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ BADFILEFLOATSIZE**
</dt> <dd>

El tamaño del archivo no es el esperado.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ BADFILETYPE**
</dt> <dd>

El archivo tiene un formato no válido.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ BADFILEVERSION**
</dt> <dd>

El archivo tiene una versión de formato no válida.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ BADOBJECT**
</dt> <dd>

Los datos no se pudieron leer o escribir en un objeto.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ BADRESOURCE**
</dt> <dd>

No se pudo realizar una operación en un recurso.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ BADTYPE**
</dt> <dd>

El archivo no coincidía con los tipos de plantilla conocidos.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ BADVALUE**
</dt> <dd>

Una variable está fuera del intervalo esperado; se devuelve normalmente cuando un puntero de objeto no es válido.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR \_ FILENOTFOUND**
</dt> <dd>

No se encontró un identificador válido para el archivo especificado.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ NOMOREDATA**
</dt> <dd>

Desplazamiento del puntero extendido más allá del final del búfer.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ NOMOREOBJECTS**
</dt> <dd>

No hay más objetos secundarios disponibles.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ NOTDONEYET**
</dt> <dd>

El tipo de datos no coincide con los tipos permitidos.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NOTFOUND**
</dt> <dd>

No se encontró el objeto a partir de los parámetros especificados.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR \_ Nº**
</dt> <dd>

No se pudo analizar el flujo de datos.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**D3DXFERR \_ RESOURCENOTFOUND**
</dt> <dd>

No se encontró un identificador válido para el recurso especificado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El código de la instalación de errores del archivo. x \_ FACD3DXF se usa para generar códigos de error. Por ejemplo:


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




