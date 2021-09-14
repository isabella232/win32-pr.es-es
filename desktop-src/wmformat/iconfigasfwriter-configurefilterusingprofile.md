---
title: Método IConfigAsfWriter ConfigureFilterUsingProfile
description: El método ConfigureFilterUsingProfile es la manera recomendada de establecer un perfil. Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Formato multimedia de windows del método ConfigureFilterUsingProfile
- Método ConfigureFilterUsingProfile windows Media Format , interfaz IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , ConfigureFilterUsingProfile (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359916"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>IConfigAsfWriter::ConfigureFilterUsingProfile (método)

El **método ConfigureFilterUsingProfile** es la manera recomendada de establecer un perfil. Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProfile* \[ En\]
</dt> <dd>

Puntero a la [**interfaz IWMProfile**](iwmprofile.md) en el perfil definido por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                         | Descripción                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>                              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>           | El **puntero de interfaz IWMProfile** no es válido.<br/> |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl> | El gráfico se detiene.<br/>                              |



 

## <a name="remarks"></a>Observaciones

Si se realiza correctamente, este método hará que se envíe un evento **\_ EC GRAPH \_ CHANGED** a la aplicación. Use este método para configurar el escritor con un perfil personalizado de la serie Windows Media 9 que ha creado (o cargado desde un archivo .prx existente) mediante los métodos del SDK de formato multimedia de Windows.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

