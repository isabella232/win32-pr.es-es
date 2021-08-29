---
title: Método IWMDRMSecurity GetContentEnablersForRevocations (Wmdrmsdk.h)
description: El método GetContentEnablersForRevocations recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Método GetContentEnablersForRevocations windows Media Format
- Método GetContentEnablersForRevocations formato multimedia de windows, interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , GetContentEnablersForRevocations method
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
ms.openlocfilehash: 60b7e998871dc64e21d0d63535228cc007cc923f6e3cc0f92e691f1f685fbe08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110315"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>Método IWMDRMSecurity::GetContentEnablersForRevocations

El **método GetContentEnablersForRevocations** recupera interfaces de habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.

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

*rgpbCerts* \[ En\]
</dt> <dd>

Matriz de certificados para los que se recuperarán los habilitadores de contenido. CCerts debe especificar el número de elementos de la *matriz.*

</dd> <dt>

*rgpdwCertSizes* \[ En\]
</dt> <dd>

Matriz que contiene los tamaños de los certificados de la *matriz rgpbCerts.* CCerts debe especificar el número de elementos de la *matriz.*

</dd> <dt>

*rgpguidCerts* \[ En\]
</dt> <dd>

Matriz que contiene los tipos de los certificados de la *matriz rgpbCerts.* CCerts debe especificar el número de elementos de la *matriz.* Para cada elemento de la matriz, use uno de los siguientes valores.



| Constante GUID                 | Descripción                                                    |
|-------------------------------|----------------------------------------------------------------|
| APLICACIÓN WMDRM \_ \_ REVOCATIONTYPE    | Especifica un certificado de aplicación.                          |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Especifica un certificado de dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Especifica un certificado Windows DRM multimedia para dispositivos de red. |



 

</dd> <dt>

*cCerts* \[ En\]
</dt> <dd>

Número de certificados para los que se recuperarán los habilitadores de contenido. Este es el número de elementos de la matriz *rgpbCerts,* la matriz *rgpdwCertSizes* y la *matriz rgpguidCerts.*

</dd> <dt>

*hResultHint* \[ En\]
</dt> <dd>

Valor devuelto recibido de la operación que ha producido un error debido a un certificado revocado. Si no llama a en respuesta a una llamada de método con error, establezca en S \_ OK.

</dd> <dt>

*prgContentEnablers* \[ out\]
</dt> <dd>

Matriz que recibe las direcciones de las interfaces **DESCONTENTENABLER** recién creadas. Establezca en **NULL** para obtener el número de habilitadores de contenido en el *parámetro pcContentEnablers.*

</dd> <dt>

*pcContentEnablers* \[ in, out\]
</dt> <dd>

Número de elementos de la *matriz prgContentEnablers.* Si *prgContentEnablers es* **NULL,** este valor se establece en el número de habilitadores de contenido necesarios en la salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Si usa la interfaz **IMFContentEnabler** para renovar los componentes revocados, debe aclarar el proceso al usuario. Esta aclaración debe hacerse porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.

Cuando se llama **a IMFContentEnabler::AutomaticEnable**, el habilitador de contenido inicia el explorador predeterminado con la dirección del servicio de actualización en el sitio web de Microsoft. Se envía al servicio de actualización un identificador único que identifica el componente revocado. A continuación, el servicio redirige el explorador a una página web desde la que el usuario puede descargar e instalar la nueva versión del componente revocado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Revocación y renovación automatizadas de componentes**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> </dl>

 

 





