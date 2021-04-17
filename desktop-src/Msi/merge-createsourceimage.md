---
description: El método CreateSourceImage del objeto Merge permite al cliente extraer los archivos de un módulo en una imagen de origen en disco después de una combinación, teniendo en cuenta los cambios realizados en el módulo que podrían haberse realizado durante la configuración del módulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Método Merge. CreateSourceImage (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670801"
---
# <a name="mergecreatesourceimage-method"></a>Merge. CreateSourceImage (método)

El método **CreateSourceImage** del objeto [**Merge**](merge-object.md) permite al cliente extraer los archivos de un módulo en una imagen de origen en disco después de una combinación, teniendo en cuenta los cambios realizados en el módulo que podrían haberse realizado durante la configuración del módulo. La lista de archivos que se van a extraer se toma de la tabla de archivos del módulo durante el proceso de mezcla. La lista de archivos se compone de todos los archivos copiados correctamente de la tabla de archivos del módulo en la base de datos de destino. Las entradas de la tabla de archivos que no se copiaron debido a conflictos de clave principal con las filas existentes en la base de datos no forman parte de esta lista. En el momento de la creación de la imagen, el directorio de cada uno de estos archivos procede de la base de datos abierta (posterior a la mezcla). La ruta de acceso especificada en el parámetro *path* es la raíz de la imagen de origen de la instalación. *fLongFileNames* determina si se usan nombres de archivo largos para los segmentos de ruta de acceso y los nombres de archivo finales. Se produce un error en la función si no hay ninguna base de datos abierta, no hay ningún módulo abierto o no se ha realizado ninguna combinación.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* 
</dt> <dd>

La ruta de acceso de la raíz de la imagen de origen para la instalación.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames* determina si se usan nombres de archivo largos para los segmentos de ruta de acceso y los nombres de archivo finales.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Esta es una lista de rutas de acceso completas para los archivos que se extrajeron correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se sobrescriben los archivos del directorio de destino con el mismo nombre. Si aún no existe, se crea la ruta de acceso.

### <a name="c"></a>C++

Consulte función [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




