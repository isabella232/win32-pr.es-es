---
title: Método ExecuteSQLQuery de ISearchDesktop
description: Toma un puntero a una cadena que contiene una consulta Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto devuelto.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- ExecuteSQLQuery method Legacy Windows Environment Features
- ExecuteSQLQuery method Legacy Windows Environment Features , ISearchDesktop interface
- ISearchDesktop interface Legacy Windows Environment Features , ExecuteSQLQuery method
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014295"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop::ExecuteSQLQuery (método)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Toma un puntero a una cadena que contiene una consulta Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto devuelto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwAttributes* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR \***

Cadena que contiene los demás atributos de la consulta.

</dd> <dt>

*pwszURL* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Cadena que contiene la SQL consulta.

</dd> <dt>

*ppidUrl* \[ out\]
</dt> <dd>

Tipo: **ppidUrl \***

Cuando este método se devuelve correctamente, contiene un puntero al conjunto de registros devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

 

 




