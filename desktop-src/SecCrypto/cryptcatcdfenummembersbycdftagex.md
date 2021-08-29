---
description: Enumera los miembros de archivo individuales en la sección CatalogFiles de un archivo de definición de catálogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Función CryptCATCDFEnumMembersByCDFTagEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 135097129067eebe95404358d2db12da87d51013bb1e959e30b613bc2a8b7653
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876385"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>Función CryptCATCDFEnumMembersByCDFTagEx

\[La **función CryptCATCDFEnumMembersByCDFTagEx** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **función CryptCATCDFEnumMembersByCDFTagEx** enumera los miembros de archivo individuales en la sección **CatalogFiles** de un archivo de definición de catálogo (CDF). **MakeCat llama a CryptCATCDFEnumMembersByCDFTagEx.** [](makecat.md)

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCDF* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRYPTCATCDF.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)

</dd> <dt>

*pwszPrevCDFTag* \[ in, out\]
</dt> <dd>

Puntero a una **cadena terminada** en NULL que identifica el miembro de archivo de catálogo.

</dd> <dt>

*pfnParseError* \[ En\]
</dt> <dd>

Puntero a una función definida por el usuario para controlar los errores de análisis de archivos.

</dd> <dt>

*ppMember* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contiene la información del miembro de archivo.

</dd> <dt>

*fContinueOnError* \[ En\]
</dt> <dd>

Valor que especifica si se debe mantener en memoria una referencia al último miembro enumerado.

</dd> <dt>

*pvReserved* \[ En\]
</dt> <dd>

Este parámetro está reservado; no lo use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se completa correctamente, esta función devuelve un puntero a una cadena terminada en **NULL** que identifica un miembro de archivo en la **sección CatalogFiles** de una CDF. La **función CryptCATCDFEnumMembersByCDFTagEx** devuelve un puntero **NULL** si se produce un error.

## <a name="remarks"></a>Comentarios

Normalmente se llama a esta función en un bucle para enumerar todos los miembros del archivo de catálogo en una CDF. Antes de entrar en el bucle, establezca *pwszPrevCDFTag en* **NULL.** La función devuelve un puntero al primer miembro. Establezca *pwszPrevCDFTag en* el valor devuelto de la función para las iteraciones posteriores del bucle.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la secuencia correcta de asignaciones para el *parámetro pwszPrevCDFTag* ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
