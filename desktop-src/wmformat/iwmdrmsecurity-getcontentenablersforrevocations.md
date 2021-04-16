---
title: Método IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: El método GetContentEnablersForRevocations recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Método GetContentEnablersForRevocations formato de Windows Media
- Método GetContentEnablersForRevocations formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649760"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>IWMDRMSecurity:: GetContentEnablersForRevocations (método)

El método **GetContentEnablersForRevocations** recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rgpbCerts* \[ de\]
</dt> <dd>

Matriz de certificados para los que se van a recuperar los habilitadores de contenido. El número de elementos de la matriz debe especificarse mediante *cCerts*.

</dd> <dt>

*rgpdwCertSizes* \[ de\]
</dt> <dd>

Matriz que contiene los tamaños de los certificados en la matriz *rgpbCerts* . El número de elementos de la matriz debe especificarse mediante *cCerts*.

</dd> <dt>

*rgpguidCerts* \[ de\]
</dt> <dd>

Matriz que contiene los tipos de los certificados de la matriz *rgpbCerts* . El número de elementos de la matriz debe especificarse mediante *cCerts*. Para cada elemento de la matriz, use uno de los valores siguientes.



| Constante GUID                 | Descripción                                                    |
|-------------------------------|----------------------------------------------------------------|
| \_aplicación REVOCATIONTYPE de WMDRM \_    | Especifica un certificado de aplicación.                          |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Especifica un certificado de dispositivo.                                |
| \_CARDEA REVOCATIONTYPE \_ WMDRM | Especifica un certificado DRM de Windows Media para dispositivos de red. |



 

</dd> <dt>

*cCerts* \[ de\]
</dt> <dd>

Número de certificados para los que se van a recuperar los habilitadores de contenido. Este es el número de elementos de la matriz *rgpbCerts* , la matriz *rgpdwCertSizes* y la matriz *rgpguidCerts* .

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

[**Revocación y renovación de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





