---
description: Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se usará para los accesos directos anunciados y los servidores OLE. Vea Limitaciones de OLE Secuencias.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabla de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00205ede9accf4ae6394a6f00bc6ae6ad54a19c5540159f57498ac5066984ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894195"
---
# <a name="icon-table"></a>Tabla de iconos

Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se usará para los accesos directos anunciados y los servidores OLE. Vea [Limitaciones de OLE Secuencias](ole-limitations-on-streams.md).

La tabla Icon tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Nombre   | [Identificador](identifier.md) | Y   | N        |
| Datos   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del archivo de icono.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Los datos del icono binario en formato PE (.dll o .exe) o icono (.ico).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se hace referencia a esta tabla cuando se ejecuta la [acción PublishProduct.](publishproduct-action.md)

Los iconos de accesos directos, extensiones de nombre de archivo y CLID deben almacenarse en archivos independientes del propio archivo de destino. Esto es necesario porque el instalador debe copiar solo los archivos de icono pequeños en la máquina del usuario al anunciar el recurso. Por lo tanto, un desarrollador de un paquete de instalación debe crear archivos independientes que contengan solo los iconos. Estos archivos de icono se almacenan como datos binarios en la tabla Icono.

Los archivos de icono que están asociados estrictamente a extensiones de nombre de archivo o CLID pueden tener cualquier extensión, como .ico. Sin embargo, los archivos de icono asociados a los accesos directos deben estar en el formato binario EXE y deben tener un nombre para que su extensión coincida con la extensión del destino. El acceso directo no funcionará si no se sigue esta regla. Por ejemplo, si un acceso directo apunta a un recurso que tiene el archivo de clave Red.bar, el archivo de icono también debe tener la extensión .bar. Se pueden agregar varios iconos al mismo archivo de icono, siempre y cuando todos los archivos de destino tengan la misma extensión.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



