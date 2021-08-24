---
description: Crea un nuevo catálogo personalizado en el indexador Windows Search y devuelve una referencia a él.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: ISearchManager2::CreateCatalog (método)
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
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597755"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2::CreateCatalog (método)

Crea un nuevo catálogo personalizado en el indexador Windows Search y devuelve una referencia a él.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszCatalog* \[ En\]
</dt> <dd>

Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nombre del catálogo que se creará. Puede ser cualquier nombre seleccionado por el autor de la llamada, solo debe contener caracteres alfanuméricos estándar y caracteres de subrayado.

</dd> <dt>

*ppCatalogManager* \[ out\]
</dt> <dd>

Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Si se realiza correctamente, se devuelve una referencia al catálogo creado como puntero de [**interfaz ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Se debe llamar a Release() en esta interfaz después de que la aplicación que realiza la llamada haya terminado de usarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

HRESULT que indica el estado de la operación:



| Código devuelto                                                                             | Descripción                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | El catálogo no existía previamente y se creó. Referencia al catálogo devuelto.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Catálogo que existía anteriormente, referencia al catálogo devuelto.<br/>                       |



 

FAILED HRESULT: error al crear el catálogo o se han pasado argumentos no válidos.

## <a name="remarks"></a>Comentarios

Se llama para crear un nuevo catálogo en el indexador Windows Search. Después de la creación, los métodos del administrador de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) devuelto se pueden usar para agregar ubicaciones para indexar, supervisar el proceso de indexación y construir consultas para enviar al indexador y obtener resultados. Consulte la documentación "Administración del índice" para obtener más información: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
