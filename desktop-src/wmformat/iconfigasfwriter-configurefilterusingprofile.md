---
title: IConfigAsfWriter ConfigureFilterUsingProfile, método
description: El método ConfigureFilterUsingProfile es la forma recomendada para establecer un perfil. Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Método ConfigureFilterUsingProfile formato de Windows Media
- Método ConfigureFilterUsingProfile formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705017"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>IConfigAsfWriter:: ConfigureFilterUsingProfile (método)

El método **ConfigureFilterUsingProfile** es la forma recomendada para establecer un perfil. Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProfile* \[ de\]
</dt> <dd>

Puntero a la interfaz [**IWMProfile**](iwmprofile.md) en el perfil definido por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                         | Descripción                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>                              |
| <dl> <dt>**\_puntero E**</dt> </dl>           | El puntero de la interfaz **IWMProfile** no es válido.<br/> |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl> | El gráfico está detenido.<br/>                              |



 

## <a name="remarks"></a>Observaciones

Si se realiza correctamente, este método hará que se envíe un evento de **\_ \_ cambio de gráfico de EC** a la aplicación. Use este método para configurar el escritor con un perfil de la serie de Windows Media 9 personalizado que haya creado (o cargado desde un archivo. prx existente) mediante los métodos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

