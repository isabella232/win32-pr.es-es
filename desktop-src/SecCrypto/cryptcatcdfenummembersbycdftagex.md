---
description: Enumera los miembros de archivo individuales de la sección CatalogFiles de un archivo de definición de catálogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx función)
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
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541003"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>CryptCATCDFEnumMembersByCDFTagEx función)

\[La función **CryptCATCDFEnumMembersByCDFTagEx** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La función **CryptCATCDFEnumMembersByCDFTagEx** enumera los miembros de archivo individuales en la sección **CatalogFiles** de un archivo de definición de catálogo (CDF). [MakeCat](makecat.md)llama a **CryptCATCDFEnumMembersByCDFTagEx** .

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*pCDF* \[ de\]
</dt> <dd>

Puntero a una estructura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszPrevCDFTag* \[ in, out\]
</dt> <dd>

Puntero a una cadena terminada en **null** que identifica el miembro del archivo de catálogo.

</dd> <dt>

*pfnParseError* \[ de\]
</dt> <dd>

Puntero a una función definida por el usuario para controlar los errores de análisis de archivos.

</dd> <dt>

*ppMember* \[ de\]
</dt> <dd>

Puntero a una estructura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contiene la información del miembro de archivo.

</dd> <dt>

*fContinueOnError* \[ de\]
</dt> <dd>

Valor que especifica si se debe mantener en memoria una referencia al último miembro enumerado.

</dd> <dt>

*pvReserved* \[ de\]
</dt> <dd>

Este parámetro está reservado; no lo utilice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se realiza correctamente, esta función devuelve un puntero a una cadena terminada en **null** que identifica un miembro de archivo en la sección **CATALOGFILES** de un CDF. La función **CryptCATCDFEnumMembersByCDFTagEx** devuelve un puntero **null** si se produce un error.

## <a name="remarks"></a>Observaciones

Normalmente, se llama a esta función en un bucle para enumerar todos los miembros del archivo de catálogo en un CDF. Antes de entrar en el bucle, establezca *pwszPrevCDFTag* en **null**. La función devuelve un puntero al primer miembro. Establezca *pwszPrevCDFTag* en el valor devuelto de la función para las iteraciones posteriores del bucle.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la secuencia correcta de asignaciones para el parámetro *pwszPrevCDFTag* ( `pwszMemberTag` ).


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
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

 

 
