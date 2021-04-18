---
title: Método GetObjectDataOnClearChannel
description: El método GetObjectDataOnClearChannel transfiere de nuevo un bloque de datos de objeto de un canal claro a Windows Media Administrador de dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel de Windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698518"
---
# <a name="getobjectdataonclearchannel-method"></a>Método GetObjectDataOnClearChannel

El método **GetObjectDataOnClearChannel** transfiere de nuevo un bloque de datos de objeto de un canal claro a Windows Media administrador de dispositivos.

Este método es idéntico a [**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , salvo que los datos devueltos por este método no están cifrados. Por consiguiente, este método es más eficaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* 
</dt> <dd>

Puntero al objeto de dispositivo.

</dd> <dt>

*pData* 
</dt> <dd>

Puntero a un búfer para recibir datos.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Puntero a un **valor DWORD** que contiene el tamaño de la transferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error en el método, devuelve un código de error **HRESULT** .



| Código devuelto                                                                                                | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_error de \_ comprobación de Mac \_ \_ de WMDM**</dt> </dl> | El código de autenticación del mensaje no es válido.<br/>                                    |
| <dl> <dt>**\_E/s de WMDM \_**</dt> </dl>           | El autor de la llamada no tiene los derechos necesarios para realizar la operación solicitada.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Error en el método. Finalice la interacción con el proveedor de contenido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un parámetro es un puntero **nulo** o no válido.<br/>                                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Se ha producido un error no especificado.<br/>                                                   |



 

## <a name="remarks"></a>Observaciones

Para transferir datos, Windows Media Administrador de dispositivos llama al método [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obtener los datos del contenedor. A continuación, se llama a **GetObjectDataOnClearChannel** para transferir bloques de datos de objeto del proveedor de contenido a Windows Media administrador de dispositivos. Si \_ se devuelve S OK con *pdwSize* establecido en cero, Windows Media administrador de dispositivos no solicitará más datos.

Este método es idéntico a [**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , salvo que los datos devueltos por este método no están cifrados. Por consiguiente, este método es más eficaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMSCP. idl</dt> </dl>    |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interfaz ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





