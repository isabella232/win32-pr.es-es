---
title: ISearchDesktop ExecuteSQLQuery, método
description: Toma un puntero a una cadena que contiene una consulta de Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto de valores devueltos.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Método ExecuteSQLQuery características del entorno heredado de Windows
- Método ExecuteSQLQuery características de entorno heredado de Windows, interfaz ISearchDesktop
- Interfaz ISearchDesktop características del entorno heredado de Windows, método ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789154"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop:: ExecuteSQLQuery (método)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Toma un puntero a una cadena que contiene una consulta de Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto de valores devueltos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwAttributes* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR \***

Cadena que contiene los demás atributos de la consulta.

</dd> <dt>

*pwszURL* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Cadena que contiene la consulta SQL.

</dd> <dt>

*ppidUrl* \[ enuncia\]
</dt> <dd>

Tipo: **ppidUrl \***

Cuando este método se devuelve correctamente, contiene un puntero al conjunto de registros devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

 

 




