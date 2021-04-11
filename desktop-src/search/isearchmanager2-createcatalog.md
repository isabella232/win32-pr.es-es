---
description: Crea un nuevo catálogo personalizado en el indizador de Windows Search y devuelve una referencia a él.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2:: CreateCatalog (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275256"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2:: CreateCatalog (método)

Crea un nuevo catálogo personalizado en el indizador de Windows Search y devuelve una referencia a él.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszCatalog* \[ de\]
</dt> <dd>

Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nombre del catálogo que se va a crear. Puede ser cualquier nombre seleccionado por el autor de la llamada, solo debe contener caracteres alfanuméricos estándar y un carácter de subrayado.

</dd> <dt>

*ppCatalogManager* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Si se ejecuta correctamente, se devuelve una referencia al catálogo creado como un puntero de interfaz [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Se debe llamar a la versión () en esta interfaz después de que la aplicación que realiza la llamada haya terminado de usarla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

HRESULT que indica el estado de la operación:



| Código devuelto                                                                             | Descripción                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | El catálogo no existía anteriormente y se creó. Referencia al catálogo devuelta.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | El catálogo existía anteriormente, se devolvió una referencia al catálogo.<br/>                       |



 

ERROR HRESULT: error al crear el catálogo o argumentos no válidos pasados.

## <a name="remarks"></a>Observaciones

Se llama para crear un nuevo catálogo en el indizador de Windows Search. Después de la creación, se pueden usar los métodos del administrador de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) devuelto para agregar ubicaciones que se van a indexar, supervisar el proceso de indexación y crear consultas para enviarlas al indexador y obtener los resultados. Consulte la documentación sobre la administración del índice para obtener más información: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
