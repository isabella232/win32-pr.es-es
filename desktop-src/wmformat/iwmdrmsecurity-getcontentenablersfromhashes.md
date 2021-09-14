---
title: Método IWMDRMSecurity GetContentEnablersFromHashes (Wmdrmsdk.h)
description: El método GetContentEnablersFromHashes recupera interfaces de habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Método GetContentEnablersFromHashes windows Media Format
- Método GetContentEnablersFromHashes windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , GetContentEnablersFromHashes (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251451"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>Método IWMDRMSecurity::GetContentEnablersFromHashes

El **método GetContentEnablersFromHashes** recupera interfaces de habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.

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

*rgpbCertHashes* \[ En\]
</dt> <dd>

Matriz de hashes de certificado para los que se obtienen los habilitadores de contenido.

</dd> <dt>

*cCerts* \[ En\]
</dt> <dd>

Número de certificados para los que se recuperan los habilitadores de contenido. Este es el número de elementos de la *matriz rgpbCertHashes.*

</dd> <dt>

*hResultHint* \[ En\]
</dt> <dd>

Valor devuelto recibido de la operación que ha producido un error debido a un certificado revocado. Si no llama a en respuesta a una llamada de método con error, establezca en S \_ OK.

</dd> <dt>

*prgContentEnablers* \[ out\]
</dt> <dd>

Matriz que recibe las direcciones de las interfaces **DESCONTENTContentEnabler** recién creadas. Establezca en **NULL** para obtener el número de habilitadores de contenido en el *parámetro pcContentEnablers.*

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



 

## <a name="remarks"></a>Observaciones

Si usa la interfaz **IMFContentEnabler** para renovar los componentes revocados, debe aclarar el proceso al usuario. Esta aclaración debe realizarse porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.

Cuando se llama **a IMFContentEnabler::AutomaticEnable**, el habilitador de contenido inicia el explorador predeterminado con la dirección del servicio de actualización en el sitio web de Microsoft. Se envía al servicio de actualización un identificador único que identifica el componente revocado. A continuación, el servicio redirige el explorador a una página web desde la que el usuario puede descargar e instalar la nueva versión del componente revocado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





