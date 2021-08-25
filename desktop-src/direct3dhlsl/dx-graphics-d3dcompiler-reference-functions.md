---
title: Funciones del compilador (referencia hlsl)
description: Esta sección contiene información sobre las siguientes funciones del compilador HLSL de Direct3D
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- functions, Compiler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465812"
---
# <a name="compiler-functions-hlsl-reference"></a>Funciones del compilador (referencia hlsl)

Esta sección contiene información sobre las siguientes funciones del compilador HLSL de Direct3D:

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | Obtiene un puntero a una interfaz de reflexión.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | Compile código HLSL o un archivo de efecto en código de bytes para un destino determinado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | Compila código de Lenguaje de sombreador de alto nivel (HLSL) de Microsoft en código de bytes para un destino determinado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store. Consulte la sección "Compilación de sombreadores para UWP", en los comentarios de <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> Compila código HLSL en código de bytes para un destino determinado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store.</blockquote><br /> Comprime un conjunto de sombreadores en un formato más compacto. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | Crea un búfer.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | Crea una interfaz function-linking-graph. <br /><blockquote>[!Note]<br />Esta función forma parte de la tecnología de vinculación de sombreadores HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlos en bibliotecas y vincularlos a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | Crea una interfaz del vinculador. <br /><blockquote>[!Note]<br />Esta función forma parte de la tecnología de vinculación de sombreadores HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlos en bibliotecas y vincularlos a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store.</blockquote><br /> Descomprime uno o varios sombreadores de un conjunto comprimido. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | Desensambla el código HLSL compilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | Desensambla el código HLSL compilado de un efecto Direct3D10.<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | Desensambla una sección del código HLSL compilado que se especifica mediante los pasos de seguimiento del sombreador.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | Desensambla una región específica del código HLSL compilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | Recupera una parte específica de un resultado de compilación.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store.</blockquote><br /> Obtiene información de depuración del sombreador.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> puede modificarse o no estar disponible para las versiones después de Windows 8.1. En su <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>lugar, use D3DGetBlobPart</strong></a> con <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>el D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> valor.</blockquote><br /> Obtiene las firmas de entrada y salida de un resultado de compilación.<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> puede modificarse o no estar disponible para las versiones después de Windows 8.1. En su <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>lugar, use D3DGetBlobPart</strong></a> con <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>el D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> valor.</blockquote><br /> Obtiene la firma de entrada de un resultado de compilación.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> puede modificarse o no estar disponible para las versiones después de Windows 8.1. En su <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>lugar, use D3DGetBlobPart</strong></a> con <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> valor.</blockquote><br /> Obtiene la firma de salida de un resultado de compilación.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | Recupera los desplazamientos de bytes para obtener instrucciones dentro de una sección del código del sombreador.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | Crea una interfaz de módulo de sombreador a partir de datos de origen para el módulo del sombreador. <br /><blockquote>[!Note]<br />Esta función forma parte de la tecnología de vinculación de sombreadores HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlos en bibliotecas y vincularlos a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | Preprocesa código HLSL nocompilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store.</blockquote><br /> Lee un archivo que está en el disco en memoria.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | Obtiene un puntero a una interfaz de reflexión.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | Crea una interfaz de reflexión de biblioteca a partir de datos de origen que contiene una biblioteca HLSL de funciones. <br /><blockquote>[!Note]<br />Esta función forma parte de la tecnología de vinculación de sombreadores HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlos en bibliotecas y vincularlos a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | Establece información en un resultado de compilación.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | Quita los blobs no deseados de un resultado de compilación.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />Puede usar esta API para desarrollar aplicaciones de Windows Store, pero no puede usarla en aplicaciones que envíe a Windows Store.</blockquote><br /> Escribe un blob en memoria en un archivo en el disco.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

