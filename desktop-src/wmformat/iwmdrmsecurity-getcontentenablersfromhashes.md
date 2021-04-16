---
title: Método IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: El método GetContentEnablersFromHashes recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Método GetContentEnablersFromHashes formato de Windows Media
- Método GetContentEnablersFromHashes formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649577"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>IWMDRMSecurity:: GetContentEnablersFromHashes (método)

El método **GetContentEnablersFromHashes** recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rgpbCertHashes* \[ de\]
</dt> <dd>

Matriz de hash de certificado para el que se van a obtener habilitadores de contenido.

</dd> <dt>

*cCerts* \[ de\]
</dt> <dd>

Número de certificados para los que se van a recuperar los habilitadores de contenido. Es el número de elementos de la matriz *rgpbCertHashes* .

</dd> <dt>

*hResultHint* \[ de\]
</dt> <dd>

Valor devuelto recibido de la operación que produjo un error debido a un certificado revocado. Si no llama a en respuesta a una llamada al método con errores, establezca en es \_ correcto.

</dd> <dt>

*prgContentEnablers* \[ enuncia\]
</dt> <dd>

Matriz que recibe las direcciones de las interfaces **IMFContentEnabler** recién creadas. Establezca en **null** para obtener el número de habilitadores de contenido en el parámetro *pcContentEnablers* .

</dd> <dt>

*pcContentEnablers* \[ in, out\]
</dt> <dd>

Número de elementos de la matriz *prgContentEnablers* . Si *prgContentEnablers* es **null**, este valor se establece en el número de habilitadores de contenido necesarios en la salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si usa la interfaz **IMFContentEnabler** para renovar los componentes revocados, debe aclarar el proceso al usuario. Esta Aclaración debe realizarse porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.

Cuando se llama a **IMFContentEnabler:: AutomaticEnable**, el habilitador de contenido inicia el explorador predeterminado con la dirección del servicio de actualización en el sitio web de Microsoft. Un identificador único que identifica el componente revocado se envía al servicio de actualización. A continuación, el servicio redirige el explorador a una página web desde la que el usuario puede descargar e instalar la nueva versión del componente revocado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





